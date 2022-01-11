# Jungle

An e-commerce application built with Rails 4.2 for purposes of teaching Rails by example, by Lighthouse Labs. I added features, fixed bugs and upgraded the user-interface design of this existing web application in order to learn the Rails framework.

## Features Added

- "Sold Out" badge for products out of stock
- Administrator page for adding new product categories
- Added user authentication
- Added order details to summarize purchase after payment

## Bugs Fixed

- Money formatting (fixed decimal points and leading '$' signs)
- Fixed basic http authentication for administrators
- Fixed empty cart checkout

## RSpec Testing

- Home page functionality
- Product details page functionality
- Add-to-cart functionality

## UI Upgrade

### Original UI:

![Original UI](public/screenshots/original-ui.jpeg)

### Upgraded UI:

![Upgraded UI](public/screenshots/upgraded-ui.jpeg)

# Demo

![Main Links Demo](public/gifs/20220110231106732.gif)
![Login & Signup Demo](public/gifs/login-signup.gif)

## Setup

## Additional Steps for Apple M1 Machines

1. Make sure that you are runnning Ruby 2.6.6 (`ruby -v`)
1. Install ImageMagick `brew install imagemagick imagemagick@6 --build-from-source`
1. Remove Gemfile.lock
1. Replace Gemfile with version provided [here](https://gist.githubusercontent.com/FrancisBourgouin/831795ae12c4704687a0c2496d91a727/raw/ce8e2104f725f43e56650d404169c7b11c33a5c5/Gemfile)

## General Setup

1. Run `bundle install` to install dependencies
2. Create `config/database.yml` by copying `config/database.example.yml`
3. Create `config/secrets.yml` by copying `config/secrets.example.yml`
4. Run `bin/rake db:reset` to create, load and seed db
5. Create .env file based on .env.example
6. Sign up for a Stripe account
7. Put Stripe (test) keys into appropriate .env vars
8. Run `bin/rails s -b 0.0.0.0` to start the server

## Stripe Testing

Use Credit Card # 4111 1111 1111 1111 for testing success scenarios.

More information in their docs: <https://stripe.com/docs/testing#cards>

## Dependencies

- Rails 4.2 [Rails Guide](http://guides.rubyonrails.org/v4.2/)
- PostgreSQL 9.x
- Stripe

## Testing

- RSpec (unit testing)
- Capybara & Poltergeist (intergration testing)
