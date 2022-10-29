# NextJS White Label

This project is an example of White Label project with NextJS. Based on NextJS template [with-docker-multi-env](https://github.com/vercel/next.js/tree/canary/examples/with-docker-multi-env).

## How to use

This project use Docker to develop, test, build and deploy main application and storybook documentation. And Makefile to automate Docker environments.

## Using Docker and Makefile

### Development environment - for local development

```bash
make build-development ## Build the development docker images
make start-development ## Start the development docker containers
make stop-development ## Stop and remove the development docker containers
```

or

```bash
make restart-development ## make stop-development && make build-development && make start-development
```

Open NextJS at http://localhost:3001 and Storybook at http://localhost:6001

### Staging environment - for doing UAT testing

```bash
make build-staging ## Build the staging docker images
make start-staging ## Start the staging docker containers
make stop-staging ## Stop and remove the staging docker containers
```

Open http://localhost:3002

### Production environment - for users

```bash
make build-production ## Build the production docker images
make start-production ## Start the production docker containers
make stop-production ## Stop and remove the production docker containers
```

Open http://localhost:3003
