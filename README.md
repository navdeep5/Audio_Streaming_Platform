# UAtify

## Table of Contents

- [Overview](#overview)
- [User Guide](#user-guide)
- [Primary Functions](#primary-functions)
- [Testing Strategy](#testing-strategy)
- [Group Work Breakdown/Responsibilities](#group-work-breakdownresponsibilities)
- [Method of Coordination](#method-of-coordination)
- [Appendix](#appendix)

## Overview

**Mini-Project-1 Design Document** outlines the implementation and functionality of a user management system developed for CMPUT 291, A1. The system consists of two main while loops: one for handling user login and registration, and another for navigating user or artist menus. The project was developed by Dylan Du, Navdeep Singh, and Ty Greve.

At a high level, the program:
- Displays a login menu where users can register or log in.
- Allows users to log in as either a regular user or an artist.
- Provides separate menus for users and artists to interact with the system.
- Cycles back to the login menu upon logging out.

## User Guide

### Starting the Program

1. **Navigate to the Directory**: Ensure the directory contains the program file and the database file (initialized with the provided schema).
2. **Run the Program**: Open the terminal and type:
    ```bash
    python3 main.py xxxx.db
    ```
   Replace `xxxx` with the name of your database file.

   In this case, you can use tables.db

### Login or Create Account

- **Login Screen**: You will see two options or can type 'q' to quit.
- **Create Account**: Type `1` and enter your username, name, and password.
- **Log In**: Type `2` and enter your username and password.
- **Main Menu**: Following successful login, you will access the main menu.

### Main Menu

- **Options**: 
  - Type `1` to start a session.
  - Type `2` to search for songs or playlists.
  - Type `3` to search for artists.
  - Type `4` to end your current session.
  - Type `q` to quit or `l` to log out.

### Searching for Songs or Playlists

- **Enter Keywords**: Provide keywords related to the songs or playlists.
- **Navigate Results**: Type `n` for next page, the number above a song/playlist for more details, or `q` to return to the main menu.
- **Song Actions**: After selecting a song or playlist, you can listen, get info, or add a song to a playlist.

### Searching for Artists

- **Enter Keywords**: Provide keywords related to the artists or their songs.
- **Navigate Results**: Type `n` for next page, the number above an artist for more details, or `q` to return to the main menu.

### Selecting an Artist’s Discography

- **View Songs**: See all songs performed by an artist.
- **Song Actions**: Listen to, get info about, or add a song to a playlist.

### Adding a Song to a Playlist

- **Select Playlist**: Choose from existing playlists or type `new` to create a new playlist and add the song.

## Primary Functions

### process_login(option)

- **Purpose**: Processes user input during login or registration.
- **Parameters**: `option` - a string indicating "User/Artist login" or "Register User".
- **Functionality**: Prompts for username/password and calls `database_functions.py` for authentication tasks.

### song_actions(songs, uid)

- **Purpose**: Provides an interface for song-related actions.
- **Parameters**: `songs` - list of songs, `uid` - user ID.
- **Functionality**: Allows listening, getting info, and adding songs to playlists by interacting with `database_functions.py`.

## Testing Strategy

The code structure facilitates testing through an intermediary file, `database_functions.py`, which isolates database queries from the main interface logic.

### Steps

1. **Individual Query Testing**: Test functions in `database_functions.py` with a controlled dataset.
2. **Interface Testing**: Verify that interface interactions produce the correct queries and results.

### Example Scenarios

- Preventing empty string inputs for username/password.
- Handling incorrect input safely.
- Ensuring unique constraints for songs by title and duration.

## Group Work Breakdown/Responsibilities

1. **Dylan Du** (18 hours)
   - Login screen design and implementation
   - User and artist login processing
   - Artist actions (adding songs, finding top fans)
   - Interface design and session management

2. **Navdeep Singh** (11 hours)
   - Session start/end implementation
   - Search functionality for artists and songs/playlists
   - Song actions interface and information retrieval

3. **Ty Greve** (8 hours)
   - Song action implementation
   - Session management and user guide
   - Testing and bug identification

## Method of Coordination

- Communication through text, in-person updates, GitHub pull requests, and documentation.

## Appendix

1. **High-Level Code Representation**: Visual representation of the outer and inner while loops for login and user/artist menus.
2. **Function Flow**: Detailed depiction of the `process_login()` function and its interaction with the database.

For any inquiries or further information, please contact the project team via their respective channels.
