#Stack Overflow Clone Site

This repo contains a Rails app I built while studying at Launch Academy in Boston. The assignment was to build a website similar to [stackoverflow.com](http://stackoverflow.com/), for posting questions and answers.

**I did the exercise mainly to practice the following:**
* Building a Rails app from scratch
* Using Rails routes
* Using Rails form helpers
* Using Active Record associations

###Models 

The application should support the following user stories. Review all of the user stories before beginning to get a sense of the scope of the project. Consider how you'll structure information within the database and sketch an initial ER diagram.

Once you've reviewed the user stories below, implement **one user story at a time**. It is important to work incrementally and verify that a user story is complete before tackling the next one.

The user stories are ordered by increasing complexity and should build on top of each other. Note that the first user stories depend on viewing questions without having a form to create them. In this case you can use `rails console` or `psql rescue_mission_development` to directly add questions to the database for testing purposes.

This section of user stories can be accomplished after reading about the following (as well as previous readings):
- [Rails Requests][rails-requests]
- [Rails Forms][rails-forms]

#### View All Questions

```no-highlight
As a user
I want to view recently posted questions
So that I can help others

Acceptance Criteria

- I must see the title of each question
- I must see questions listed in order, most recently posted first
```

#### View a Question's Details

```no-highlight
As a user
I want to view a question's details
So that I can effectively understand the question

Acceptance Criteria

- I must be able to get to this page from the questions index
- I must see the question's title
- I must see the question's description
```

#### Post a Question

```no-highlight
As a user
I want to post a question
So that I can receive help from others

Acceptance Criteria

- I must provide a title that is at least 40 characters long
- I must provide a description that is at least 150 characters long
- I must be presented with errors if I fill out the form incorrectly
```

#### Answering a Question

```no-highlight
As a user
I want to answer another user's question
So that I can help them solve their problem

Acceptance Criteria

- I must be on the question detail page
- I must provide a description that is at least 50 characters long
- I must be presented with errors if I fill out the form incorrectly
```

The following section of the core user stories can be completed after reading the following article:
- [Rails Nested Routes][rails-nested-resources]

#### Viewing a Question's Answers

```no-highlight
As a user
I want to view the answers for a question
So that I can learn from the answer

Acceptance Criteria

- I must be on the question detail page
- I must only see answers to the question I'm viewing
- I must see all answers listed in order, most recent last
```

#### Editing a Question

```no-highlight
As a user
I want to edit a question
So that I can correct any mistakes or add updates

Acceptance Criteria

- I must provide valid information
- I must be presented with errors if I fill out the form incorrectly
- I must be able to get to the edit page from the question details page
```

#### Deleting a Question

```no-highlight
As a user
I want to delete a question
So that I can delete duplicate questions

Acceptance Criteria

- I must be able delete a question from the question edit page
- I must be able delete a question from the question details page
- All answers associated with the question must also be deleted
```

### Non-core User Stories

#### Markdown Support

```no-highlight
As a user
I want to write my questions and answers with markdown
So I can easily format my questions and answers

Acceptance Criteria

- I can write my questions and answers using markdown syntax
- Questions and answers, when shown, should be the HTML rendered from the
  markdown
```

#### Choosing an Answer

```no-highlight
As a user
I want to mark an answer as the best answer
So that others can quickly find the answer

Acceptance Criteria

- I must be on the question detail page
- I must be able mark an answer as the best
- I must see the "best" answer above all other answers in the answer list
```

#### User Authentication

```no-highlight
As a user
I want to sign in
So that my questions and answers can be associated to me

Acceptance Criteria

- I must be able to sign in using either GitHub, Twitter, or Facebook (choose
  one)
```

#### User Signs Out

```no-highlight
As a user
I want to be able to sign out
So that other users of my computer can't pretend to be me

Acceptance Criteria

- I must be able to sign out from any page
```

#### Prevent Users From Editing Other Another User's Questions

```no-highlight
As a user
I want to prevent other users from editing my questions
So that malicious users can't mess with my question

Acceptance Criteria

- I must be signed in
- I must be able to edit a question that I posted
- I can't edit a question that was posted by another user
```

#### Prevent Users Choosing "Best" Answer for Another User's Questions

```no-highlight
As a user
I want to prevent other users from choosing the "best" answer for my question
So that malicious users can't mess with my question

Acceptance Criteria

- I must be signed in
- I must be able to choose the "best" answer for a question that I posted
- I can't choose the best answer for a question that was posted by another user
```

#### Prevent Users Choosing Deleting Another User's Question

```no-highlight
As a user
I want to prevent other users from deleting my question
So that malicious users can't mess with my question

Acceptance Criteria

- I must be signed in
- I must be able to delete a question that I posted
- I can't delete a question that was posted by another user
```

[forms_for_models]: http://guides.rubyonrails.org/form_helpers.html#dealing-with-model-objects
[intro-to-rails]: https://learn.launchacademy.com/lessons/intro-to-rails
[rails-routes]: https://learn.launchacademy.com/lessons/rails-routes
[rails-controllers]: https://learn.launchacademy.com/lessons/rails-controllers
[rails-requests]: https://learn.launchacademy.com/lessons/rails-requests
[rails-forms]: https://learn.launchacademy.com/lessons/rails-forms
[rails-nested-resources]: https://learn.launchacademy.com/lessons/rails-nested-resources