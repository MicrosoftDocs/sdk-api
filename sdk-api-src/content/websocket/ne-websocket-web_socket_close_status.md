---
UID: NE:websocket._WEB_SOCKET_CLOSE_STATUS
title: WEB_SOCKET_CLOSE_STATUS (websocket.h)
description: Specifies the WebSocket close status.
helpviewer_keywords: ["WEB_SOCKET_ABORTED_CLOSE_STATUS","WEB_SOCKET_CLOSE_STATUS","WEB_SOCKET_CLOSE_STATUS enumeration [Websocket Protocol Component API]","WEB_SOCKET_EMPTY_CLOSE_STATUS","WEB_SOCKET_ENDPOINT_UNAVAILABLE_CLOSE_STATUS","WEB_SOCKET_INVALID_DATA_TYPE_CLOSE_STATUS","WEB_SOCKET_INVALID_PAYLOAD_CLOSE_STATUS","WEB_SOCKET_MESSAGE_TOO_BIG_CLOSE_STATUS","WEB_SOCKET_POLICY_VIOLATION_CLOSE_STATUS","WEB_SOCKET_PROTOCOL_ERROR_CLOSE_STATUS","WEB_SOCKET_SECURE_HANDSHAKE_ERROR_CLOSE_STATUS","WEB_SOCKET_SERVER_ERROR_CLOSE_STATUS","WEB_SOCKET_SUCCESS_CLOSE_STATUS","WEB_SOCKET_UNSUPPORTED_EXTENSIONS_CLOSE_STATUS","websock.web_socket_close_status","websocket/WEB_SOCKET_ABORTED_CLOSE_STATUS","websocket/WEB_SOCKET_CLOSE_STATUS","websocket/WEB_SOCKET_EMPTY_CLOSE_STATUS","websocket/WEB_SOCKET_ENDPOINT_UNAVAILABLE_CLOSE_STATUS","websocket/WEB_SOCKET_INVALID_DATA_TYPE_CLOSE_STATUS","websocket/WEB_SOCKET_INVALID_PAYLOAD_CLOSE_STATUS","websocket/WEB_SOCKET_MESSAGE_TOO_BIG_CLOSE_STATUS","websocket/WEB_SOCKET_POLICY_VIOLATION_CLOSE_STATUS","websocket/WEB_SOCKET_PROTOCOL_ERROR_CLOSE_STATUS","websocket/WEB_SOCKET_SECURE_HANDSHAKE_ERROR_CLOSE_STATUS","websocket/WEB_SOCKET_SERVER_ERROR_CLOSE_STATUS","websocket/WEB_SOCKET_SUCCESS_CLOSE_STATUS","websocket/WEB_SOCKET_UNSUPPORTED_EXTENSIONS_CLOSE_STATUS"]
old-location: websock\web_socket_close_status.htm
tech.root: WebSock
ms.assetid: bd2c279c-ae6c-469a-8a97-d46fca042126
ms.date: 12/05/2018
ms.keywords: WEB_SOCKET_ABORTED_CLOSE_STATUS, WEB_SOCKET_CLOSE_STATUS, WEB_SOCKET_CLOSE_STATUS enumeration [Websocket Protocol Component API], WEB_SOCKET_EMPTY_CLOSE_STATUS, WEB_SOCKET_ENDPOINT_UNAVAILABLE_CLOSE_STATUS, WEB_SOCKET_INVALID_DATA_TYPE_CLOSE_STATUS, WEB_SOCKET_INVALID_PAYLOAD_CLOSE_STATUS, WEB_SOCKET_MESSAGE_TOO_BIG_CLOSE_STATUS, WEB_SOCKET_POLICY_VIOLATION_CLOSE_STATUS, WEB_SOCKET_PROTOCOL_ERROR_CLOSE_STATUS, WEB_SOCKET_SECURE_HANDSHAKE_ERROR_CLOSE_STATUS, WEB_SOCKET_SERVER_ERROR_CLOSE_STATUS, WEB_SOCKET_SUCCESS_CLOSE_STATUS, WEB_SOCKET_UNSUPPORTED_EXTENSIONS_CLOSE_STATUS, websock.web_socket_close_status, websocket/WEB_SOCKET_ABORTED_CLOSE_STATUS, websocket/WEB_SOCKET_CLOSE_STATUS, websocket/WEB_SOCKET_EMPTY_CLOSE_STATUS, websocket/WEB_SOCKET_ENDPOINT_UNAVAILABLE_CLOSE_STATUS, websocket/WEB_SOCKET_INVALID_DATA_TYPE_CLOSE_STATUS, websocket/WEB_SOCKET_INVALID_PAYLOAD_CLOSE_STATUS, websocket/WEB_SOCKET_MESSAGE_TOO_BIG_CLOSE_STATUS, websocket/WEB_SOCKET_POLICY_VIOLATION_CLOSE_STATUS, websocket/WEB_SOCKET_PROTOCOL_ERROR_CLOSE_STATUS, websocket/WEB_SOCKET_SECURE_HANDSHAKE_ERROR_CLOSE_STATUS, websocket/WEB_SOCKET_SERVER_ERROR_CLOSE_STATUS, websocket/WEB_SOCKET_SUCCESS_CLOSE_STATUS, websocket/WEB_SOCKET_UNSUPPORTED_EXTENSIONS_CLOSE_STATUS
req.header: websocket.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WEB_SOCKET_CLOSE_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WEB_SOCKET_CLOSE_STATUS
 - websocket/_WEB_SOCKET_CLOSE_STATUS
 - WEB_SOCKET_CLOSE_STATUS
 - websocket/WEB_SOCKET_CLOSE_STATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Websocket.h
api_name:
 - WEB_SOCKET_CLOSE_STATUS
---

# WEB_SOCKET_CLOSE_STATUS enumeration


## -description

The <b>WEB_SOCKET_CLOSE_STATUS</b> enumeration specifies the WebSocket close status as defined by <a href="http://tools.ietf.org/html/rfc6455">WSPROTO</a>.

## -enum-fields

### -field WEB_SOCKET_SUCCESS_CLOSE_STATUS:1000

Close completed successfully.

### -field WEB_SOCKET_ENDPOINT_UNAVAILABLE_CLOSE_STATUS:1001

The endpoint is going away and thus closing the connection.

### -field WEB_SOCKET_PROTOCOL_ERROR_CLOSE_STATUS:1002

Peer detected protocol error and it is closing the connection.

### -field WEB_SOCKET_INVALID_DATA_TYPE_CLOSE_STATUS:1003

The endpoint cannot receive this type of data.

### -field WEB_SOCKET_EMPTY_CLOSE_STATUS:1005

No close status
      code was provided.

### -field WEB_SOCKET_ABORTED_CLOSE_STATUS:1006

The
      connection was closed without sending or
      receiving a close frame.

### -field WEB_SOCKET_INVALID_PAYLOAD_CLOSE_STATUS:1007

Data within a message is not consistent with the type of the message.

### -field WEB_SOCKET_POLICY_VIOLATION_CLOSE_STATUS:1008

The message violates an endpoint's policy.

### -field WEB_SOCKET_MESSAGE_TOO_BIG_CLOSE_STATUS:1009

The message sent was too large to process.

### -field WEB_SOCKET_UNSUPPORTED_EXTENSIONS_CLOSE_STATUS:1010

A client endpoint expected the server to negotiate one or more extensions, but the server didn't return them in the response message of the WebSocket handshake.

### -field WEB_SOCKET_SERVER_ERROR_CLOSE_STATUS:1011

An unexpected condition prevented the server from
      fulfilling the request.

### -field WEB_SOCKET_SECURE_HANDSHAKE_ERROR_CLOSE_STATUS:1015

The
      TLS handshake could not be completed.

## -see-also

<a href="/windows/desktop/api/websocket/ns-websocket-web_socket_buffer">WEB_SOCKET_BUFFER</a>
