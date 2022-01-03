# System Design Interviews (SDIs)

Engineers often struggle with SDIs primarily because of three reasons:

- Asked to work on an open-ded design problem that doesn't have a standard answer.

- Lack experience in developing complex and large scale systems.

- Did not spend enough time preparing for SDIs.

## Step 1: Requirements clarifications

Ask questions about the exact scope of the problem we are solving. Often, design questions are open-ended, and don't have a single correct answer. Since time is limited, it is also important to clarify which parts of the system we will be focusing on.

## Step 2: Back-of-the-envelope estimation

It's a good idea to estimate the scale of the system, this will come in handy later.

- What scale is expected from the system (e.g., number of ....)?

- How much storage will we need?

- What network bandwidth usage are we expecting?

## Step 3: System interface definition

Define what APIs are expected from the system. Helps to establish the exact contract expected from the system and will also help us ensure if we haven't gotten any requirements wrong.

## Step 4: Defining data model

Defining the data model upfront will clarify how data will flow between the different components of the systems.

Which database system should we use? Which one fits our needs the best, NoSQL or MySQL?

## Step 5: High-level design

Draw a block diagram with 5-6 boxes respresenting the core components of our system. Enough to see what is needed to solve the actual problem end-to-end.

## Step 6: Detailed design

Dig deeper into two or three major components. Talk to the interviewer, their feedback should guide us to what needs to be further discussed in the system. We should be able to speak about various approaches, pros and cons, explain why we may choose a particular approach over another for our use-case.

There is not a single right answer in SDIs.

- Since we will be storing massive amount of data, how should we partition our data to distribute it to multiple databases? Should we try to store all of the data of a user on the same database? What issue could it cause?

- How much and at which layer should we intorduce cache to speed things up?

- What components need better load balancing?

## Step 7: Identifying and resolving bottlenecks

Try to discuss as many bottlenecks as possible, and how to prevent them or recover from failures.

- Is there any single point of failure in our system? What we doing to mitigate it?

- Do we have enough replicas of the data so that if we lose a few servers, we can still server our users?

- Similarly, do we have enough copies of different services running such that a few failures will not cause total system shutdown?

- How are we monitoring the performance of our server? Do we get alerts whenever critical components fail or their performance degrades?

## Summary

Preparation and being organized during the interview are the keys to be successful in system design interviews.
