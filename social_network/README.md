# Decentralized Social Network DApp

This project is a simple decentralized social network built on top of Cartesi Rollups. The application allows users to create profiles, post messages, and view posts in a decentralized manner. This example demonstrates how to handle state updates and inspections using Cartesi Rollups.

## Features

- **Profile Creation**: Users can create profiles that store their name and bio.
- **Message Posting**: Users can post messages, which are timestamped and associated with their profile.
- **Viewing Profiles and Posts**: Users can view existing profiles and posts.

## Project Structure

- **`hex2Object` & `obj2Hex`**: Utility functions for converting between hex and JSON objects.
- **`handle_advance`**: Function to handle state updates like profile creation and message posting.
- **`handle_inspect`**: Function to handle inspection requests like viewing profiles and posts.
- **`profiles` & `posts`**: In-memory storage for user profiles and posts.

## Prerequisites

- Node.js installed on your machine.
- Cartesi Rollups environment set up.
- A running instance of a Cartesi Rollups HTTP server.

## Installation

1. **Clone the repository**:

   ```bash
   git clone https://github.com/yourusername/your-repo-name.git
   cd your-repo-name
   ```

2. **Install dependencies**:

   ```bash
   npm install
   ```

3. **Set environment variables**:

   Create a `.env` file in the root directory and add the following:

   ```env
   ROLLUP_HTTP_SERVER_URL=http://localhost:4000
   ```

4. **Start the application**:

   ```bash
   node app.js
   ```

## Usage

### Creating a Profile

To create a profile, send a request with the action `create_profile`, including the user's name and optional bio. The profile will be stored in the `profiles` array.

### Posting a Message

To post a message, send a request with the action `post_message`, including the message content. The message will be stored in the `posts` array with a timestamp.

### Viewing Profiles and Posts

To view profiles or posts, send an inspection request with the appropriate route (`profiles` or `posts`). The response will contain the relevant data in JSON format.

## Extending the Application

This DApp is a simple foundation for a decentralized social network. You can extend its functionality by adding features like:

- **Likes/Comments**: Implement a system for liking and commenting on posts.
- **Follow System**: Allow users to follow other profiles.
- **Profile Pictures**: Enable profile picture uploads using decentralized storage solutions like IPFS.