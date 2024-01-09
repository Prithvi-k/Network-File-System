# Network File System

# Setup

1. Clone this repository / Download the zip file
2. Change into the directory
3. Run `bash setup.sh` to generate test cases
4. Run `make` to compile files for naming server, storage server and client.
5. Run naming server by executing `./nm.out`, storage server by executing `./ss.out` and client by executing `./client.out`

## Makefile commands

- `make / make all` : Compiles files for naming server, storage server and client
- `make client` : Compiles only files for client
- `make naming_server / make ns / make nm` : Compiles only files for naming server
- `make storage_server / make ss` : Compiles only files for storage server
- `make clean` : Deletes compiled `.out` executables
- `make clean_test_cases` : Deletes the `test_cases` directory.
- `make clean_log` : Deletes the `log_file.txt` file.
- `make reset` : Resets the directory to initial state deleting compiled executables, generated testcases and log file.

# Tests Run

### Basic Functioning

- [x] Read files
- [x] Read large files
- [x] Write to files
- [x] Get file info
- [x] Create file
- [x] Create folder
- [x] Delete file
- [x] Delete folder
- [x] Copy File
- [x] Copy folder

### Errors to account for

- [x] Wrong path
- [x] No access

### Edge Cases (Possible)

- [x] Create already existing file
- [x] Client-side last packet
- [x] Read files > 300 MB
- [x] Copy files concurrently

# To Do:

- [x] Redundancy and backup
- [x] ACK TIMEOUT for test_cases
- [x] Creating flag for backup file to be of same name while copying
- [x] Read Ack
- [x] Error Codes (Defined but to be declared and used properly)
- [x] Testing of all components (See [Tests](#tests))
- [x] Locks for Read/Write
- [x] Listing implement
- [x] Adding a storage server if it becomes dead (re-intiallization), only Read to be implemented if server is dead
- [x] LRU Caching Testing
- [x] Error Codes implemented on client-side
- [x] Moving (Copying Directories)
- [x] Handling Error Codes in Client (For eg, I am sending UNAUTHORISED if file cannot be read or write so have to use if conditions and all)
- [x] For Handling, suggest breaking client code into files
- [x] Invalid path ke baad connection
- [x] Book Keeping
- [x] What is '/' directory when creating a file/folder?

### Some Pointers !!!

- Any use of recv should have <= in if.
- in recv or sen sizeof(\*<name_of_packet>) not general packet or anything else
- Release a lock before returning at any point

# Contributors

- [@Chetan Mahipal](https://github.com/MirageF458Italia)
- [@Kushal Shah](https://github.com/Kushal-Shah-03)
- [@Prithvi Karthik](https://github.com/Prithvi-k)
