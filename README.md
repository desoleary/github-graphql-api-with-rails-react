# Firekamp Programming Challenge

#### GitHub Omniauth Configuration

###### Create GitHub OAuth App

- Sign into GitHub via https://github.com/
- Navigate to Developer Settings https://github.com/settings/developers
- Click on "New OAuth App"
- Enter the following details:
  - Application Name e.g. firekamp
  - Homepage URL e.g. https://github.com/desoleary/firekamp-programming-challenge
  - Authorization callback URL e.g. http://127.0.0.1:3000/auth/github/callback

#### Installation

###### Configure environment variables

```bash
cp .env.example .env
```
- Fill in FIREKAMP_GITHUB_CLIENT_ID and FIREKAMP_GITHUB_CLIENT_SECRET with OAuth App values

###### Setup

```bash
$ git clone git@github.com:desoleary/firekamp-programming-challenge.git
$ cd firekamp-programming-challenge
$ bundle install
$ bin/rails db:create
$ bin/rails db:migrate
```

##### Running
```bash
$ bin/rails s -p 3001
```

#### React
- Makes use of `react-rails` gem
- Compilation and HMR is conducted with use of `shakapacker` gem

###### HMR support
`./bin/shakapacker-dev-server` # runs on port 3035

###### Component Generator
`bin/rails g react:component HelloWorld greeting:string`

#### Nice to haves
- Cypress Testing
- Better Controller Error Handling via `rescue_from Exception`
- Add ability to support multiple auth providers per user
- Integrate with nextjs
