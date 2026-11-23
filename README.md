# STOMP WebSocket Tester

A single-page tool (HTML + JavaScript, no build process or dependencies to install) for testing **STOMP over WebSocket**endpoints directly from your browser. Designed for debugging Spring Boot backends using `@MessageMapping` and `SimpMessagingTemplate`, without having to set up a client every time.

## Features

- Connect, subscribe, and send messages to any STOMP destination
    
- Optional `Authorization: Bearer <JWT>` header
    
- Color-coded log with timestamps and safe handling of received message content
    
- Visible connection status and separate STOMP/WebSocket error handling
    
- `Ctrl/Cmd + Enter` keyboard shortcut to send messages
    

## Usage

Open `index.html` in your browser, configure the fields, and click **Connect**.

|Field|Default value|
|---|---|
|URL|`ws://localhost:5010/ws`|
|Subscribe|`/topic/greetings`|
|Destination|`/app/hello`|

> If your endpoint is configured with `.withSockJS()`, use `ws://host:port/ws/websocket` to connect via native WebSocket.
> 
> If served over HTTPS, the browser requires `wss://` (except for `localhost`).

## Tech Stack

HTML5 · Vanilla JavaScript

## License

MIT