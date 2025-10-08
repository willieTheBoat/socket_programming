# Distributed File Transfer System

A high-performance client-server file transfer application built in C++ using TCP/IP sockets. This project implements a custom binary protocol for reliable file operations across networks, similar to FTP (File Transfer Protocol).

## Overview

This system consists of two main components:
- **`cxid`** - A concurrent server that handles multiple client connections using fork-based process management
- **`cxi`** - An interactive client that connects to the server and executes file transfer commands

## Features

### File Operations
- **Upload** - Transfer local files to the remote server
- **Download** - Retrieve files from the remote server  
- **Delete** - Remove files on the remote server
- **List** - View directory contents with detailed file information


### Supported Commands

| Command | Direction | Description |
|---------|-----------|-------------|
| `GET` | Client → Server | Request file download |
| `PUT` | Client → Server | Upload file to server |
| `LS` | Client → Server | List directory contents |
| `RM` | Client → Server | Delete remote file |
| `FILEOUT` | Server → Client | File data response |
| `LSOUT` | Server → Client | Directory listing response |
| `ACK` | Server → Client | Success confirmation |
| `NAK` | Server → Client | Error response with errno |
