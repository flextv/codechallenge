# Flex Code Challenge

We're excited that you want to join us at Flex!

To help you understand what kind of work you'd be doing at Flex (and to help us assess your skills), we'd like you to build a simple React Native app.

We hope this will be a fun exercise for you!

## Your task

1. Create a React Native app project
1. Create a login page with email and password fields. To test the app, use `codechallenge@sweatflex.com` and `codechallenge`.
1. After submitting the form, send a POST request to http://staging.sweatflex.com/api/v1/auth with body `{"email":"...","password":"..."}`. Don't forget to set `Accept: 'application/json'` and `'Content-Type': 'application/json'` header fields.
1. Save the `token` field from the response.
1. Fetch a list of classes using the following GraphQL query to http://staging.sweatflex.com/graphql. You'll need to include `Authorization: Bearer TOKEN` where `TOKEN` is your token from the previous step.
    ```gql
    {
      videos {
        duration(unit: MINS)
        name
        image_url
        stream_url
      }
    }
    ```
1. Display a list of these classes
1. When a user clicks a class, navigate to a class detail view.
1. On the class detail, display information about the class.
1. Allow the user to start playing the video. You can display the video in the same view, or navigate to a separate full-screen view.
1. If you have extra time, you can take inspiration from the Flex app for more features, or add any other feature you think would be useful.

## Rules

1. Fork this repo and submit the final version as a pull request. Commit as needed.
1. You can use any resource you find on the web.
1. Visual design is not rated. We have a designer for that.
1. Code design, on the other hand, is an important criterion during evaluation.
1. You shouldn't need to spend more than 2 hours on this. Most people finish within 1 hour.

## Evaluation criteria

1. Functionality
1. Code quality
1. Ability to explain your decisions in a post-challenge interview.
1. (Optional) Bonus points for tests, flow/typescript
