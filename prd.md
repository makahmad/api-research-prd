# Twitter for Kids Product Requirements (for API usability research)

## Overview
The goal is to build twitter for kids where they can share ideas and information with their friends. A parent must be involved during the setup and the parent will have monitoring capabilities.

## Problem statement 
Kids need a safe space to bounce ideas off each other outside of Discord, Fortnite and Roblox. It could be educational, informational or just fun memes. With many kids moving to homeschooling post covid, having twitter for kids will allow them to expand their social circles and make friends from kids all around the world. Even though security protocols will be put in place to ensure only children use the product, parents will always be able to monitor their kids' accounts.

## Non-Functional Requirement
  - The backend must allow for multiple types of clients
  - System must allow for network failures allowing clients to retry
  - All user journeys must be accessible through REST APIs

## User Journeys

### Parent creates an account and child account
  1. Click Sign Up on kids.twitter.com (for the purpose of this study, all parent/child actions happen on this one domain)
  2. Enter name, birthdate, email, password and a unique username (that cannot be changed)
  3. Email sent to parent for email verification
  4. Parent verifies email and then is allowed to create a child account by entering the child name, email and birthday.
  5. Child gets an email and verifies the email.
  6. Child enters a password, a unique username and signs up

### Parent can update profile
Parent can update their email and password

### Parent adds a second parent
  1. Parent invites a 2nd parent by email (for the purpose of this study, we’re limiting to 2 parents total per child)
  2. The 2nd parent clicks on the invitation link and signs up
  3. The 2nd parent can now monitor the child similar to the first parent

### Child can update profile
  1. Child can update their username (must be unique)
  2. Child can update their profile bio, email and password

### Feed displays relevant tweets based on child’s followers and interactions (likes, comments)
  1. Upon login, the child can see tweets from other children. This could be trending tweets, the child’s follower’s tweets and/or tweets from other users that the child has interacted with by liking or commenting on their tweets.
  2. The feed is an infinite scroll meaning as long as there are tweets available to surface, the child will see tweets as they scroll down. No need for functionality to scroll up to see new tweets.
  3. Child can sort tweets by most recent tweets or most relevant tweets. Assume sorting occurs on the server side.

### Child searches and follows other children
  1. Child can search for other children by name
  2. Child can follow other children

### Child creates and deletes tweets
  1. Child can create a tweet which is 140 characters (not supporting hashtags or any other media)
  2. Child can delete a tweet (however a parent should be able to monitor deleted tweets for their children)

### Child interacts with a tweet
  1. Child can Like a tweet
  2. Child can Reply (similar to commenting) to a tweet
  3. Child can re-tweet (pointer to the original tweet w/ an optional text blurb - same as resharing on LinkedIn or facebook)

### Parent monitors child account
  1. Parent can see tweets of their own child
  2. Parent can see tweets of any children following or being followed by their child
  3. Parent can see deleted tweets by their own child
  4. Parent can export their child’s tweets to a CSV file

## Assumption:
When a child grows up and has children of their own, they will create a new parent account.
