# Welcome to my blog

What are GitHub Actions and how do they work

‘GitHub Actions’ is an API that can react to any event, GitHub’s or our own events. For example, for every push event on the repository, we want our test cases to run.

For GitHub Actions to work, we need to create a .github/workflows folder. We need to create our workflows inside this folder. Let’s create push.yml. Here is what we want from our workflow:

On every push, perform these actions in the given order

    git clone the repo
    run npm install
    run npm lint
    run npm test
    build the docker image
    login to docker hub
    Push the image to docker hub

Since we have to run each of these commands inside a docker we have to declare a Dockerfile for each of these actions and run the command in those containers. This is, of course, very tedious and error-prone. Remember, GitHub Actions are code, so we can just reuse, edit and fork them as we do with any other piece of code.
