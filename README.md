# Nultr messenger

## 🖼 Screenshots

### 🔐 Login screen

![Login](iced-client/images/login.png)

### 💬 Chat screen

![Chat](iced-client/images/chat.png)

## Status
- Messenger project built for educational purposes
- ⚠️ **This project is not actively maintained.**

## Features
- Private chats (for two users)
- Realtime messages
- Realtime message status update (sent, received by server, read)
- Beaver authentication
- Users can be created using cli command with password generation

## Structure
- Client <-> server
- Everything written in Rust

### shared-lib
- For request-response route definitions using [`rust-api-kit`](https://crates.io/crates/rust-api-kit)
- Used by server to generate routes and for request-response definitions
- Used by client to use http client and for request-response definitions

### client-lib
- Library for client implementations

### iced-client
- The current GUI client using [`iced`](https://github.com/iced-rs/iced)
- (Deprecated: Dioxus client no longer maintained)

### procmacro-lib
- Shared library for macros

### server
- Backend server using [`axum`](https://crates.io/crates/axum)

## Getting started

## For server
Run:

``` bash
cargo install sea-orm-cli@1.1.0
sea-orm-cli migrate up # creates database and runs migrations
cargo run -- add-user -- first # Creates user and outputs password
cargo run -- add-user -- second # Creates user and outputs password
cargo run
```

## For client
``` bash
cargo run
```
and input server generated passwords into login form
