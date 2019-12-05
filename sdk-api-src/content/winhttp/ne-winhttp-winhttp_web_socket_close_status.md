---
UID: NE:winhttp._WINHTTP_WEB_SOCKET_CLOSE_STATUS
title: WINHTTP_WEB_SOCKET_CLOSE_STATUS (winhttp.h)
description: The WINHTTP_WEB_SOCKET_CLOSE_STATUS enumeration includes the status of a WebSocket close operation.
old-location: http\winhttp_web_socket_close_status.htm
tech.root: WinHttp
ms.assetid: d86795e4-3a30-4368-b253-1b126387efcc
ms.date: 12/05/2018
ms.keywords: WINHTTP_WEB_SOCKET_ABORTED_CLOSE_STATUS, WINHTTP_WEB_SOCKET_CLOSE_STATUS, WINHTTP_WEB_SOCKET_CLOSE_STATUS enumeration [HTTP], WINHTTP_WEB_SOCKET_EMPTY_CLOSE_STATUS, WINHTTP_WEB_SOCKET_ENDPOINT_TERMINATED_CLOSE_STATUS, WINHTTP_WEB_SOCKET_INVALID_DATA_TYPE_CLOSE_STATUS, WINHTTP_WEB_SOCKET_INVALID_UTF8_CLOSE_STATUS, WINHTTP_WEB_SOCKET_MESSAGE_TOO_BIG_CLOSE_STATUS, WINHTTP_WEB_SOCKET_POLICY_VIOLATION_CLOSE_STATUS, WINHTTP_WEB_SOCKET_PROTOCOL_ERROR_CLOSE_STATUS, WINHTTP_WEB_SOCKET_SECURE_HANDSHAKE_ERROR_CLOSE_STATUS, WINHTTP_WEB_SOCKET_SERVER_ERROR_CLOSE_STATUS, WINHTTP_WEB_SOCKET_SUCCESS_CLOSE_STATUS, WINHTTP_WEB_SOCKET_UNSUPPORTED_EXTENSIONS_CLOSE_STATUS, http.winhttp_web_socket_close_status, winhttp/WINHTTP_WEB_SOCKET_ABORTED_CLOSE_STATUS, winhttp/WINHTTP_WEB_SOCKET_CLOSE_STATUS, winhttp/WINHTTP_WEB_SOCKET_EMPTY_CLOSE_STATUS, winhttp/WINHTTP_WEB_SOCKET_ENDPOINT_TERMINATED_CLOSE_STATUS, winhttp/WINHTTP_WEB_SOCKET_INVALID_DATA_TYPE_CLOSE_STATUS, winhttp/WINHTTP_WEB_SOCKET_INVALID_UTF8_CLOSE_STATUS, winhttp/WINHTTP_WEB_SOCKET_MESSAGE_TOO_BIG_CLOSE_STATUS, winhttp/WINHTTP_WEB_SOCKET_POLICY_VIOLATION_CLOSE_STATUS, winhttp/WINHTTP_WEB_SOCKET_PROTOCOL_ERROR_CLOSE_STATUS, winhttp/WINHTTP_WEB_SOCKET_SECURE_HANDSHAKE_ERROR_CLOSE_STATUS, winhttp/WINHTTP_WEB_SOCKET_SERVER_ERROR_CLOSE_STATUS, winhttp/WINHTTP_WEB_SOCKET_SUCCESS_CLOSE_STATUS, winhttp/WINHTTP_WEB_SOCKET_UNSUPPORTED_EXTENSIONS_CLOSE_STATUS
ms.topic: enum
f1_keywords:
- winhttp/WINHTTP_WEB_SOCKET_CLOSE_STATUS
dev_langs:
- c++
req.header: winhttp.h
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- winhttp.h
api_name:
- WINHTTP_WEB_SOCKET_CLOSE_STATUS
targetos: Windows
req.typenames: WINHTTP_WEB_SOCKET_CLOSE_STATUS
req.redist: 
ms.custom: 19H1
---

# WINHTTP_WEB_SOCKET_CLOSE_STATUS enumeration


## -description


The <b>WINHTTP_WEB_SOCKET_CLOSE_STATUS</b> enumeration includes the status of a WebSocket close operation.


## -enum-fields




### -field WINHTTP_WEB_SOCKET_SUCCESS_CLOSE_STATUS

The connection closed successfully.


### -field WINHTTP_WEB_SOCKET_ENDPOINT_TERMINATED_CLOSE_STATUS

The peer is going away and terminating the connection.


### -field WINHTTP_WEB_SOCKET_PROTOCOL_ERROR_CLOSE_STATUS

A protocol error occurred.


### -field WINHTTP_WEB_SOCKET_INVALID_DATA_TYPE_CLOSE_STATUS

Invalid data received by the peer.


### -field WINHTTP_WEB_SOCKET_EMPTY_CLOSE_STATUS

The close message was empty.


### -field WINHTTP_WEB_SOCKET_ABORTED_CLOSE_STATUS

The connection was aborted.


### -field WINHTTP_WEB_SOCKET_INVALID_PAYLOAD_CLOSE_STATUS


### -field WINHTTP_WEB_SOCKET_POLICY_VIOLATION_CLOSE_STATUS

The message violates an endpoint's policy.


### -field WINHTTP_WEB_SOCKET_MESSAGE_TOO_BIG_CLOSE_STATUS

The message sent was too large to process.


### -field WINHTTP_WEB_SOCKET_UNSUPPORTED_EXTENSIONS_CLOSE_STATUS

A client endpoint expected the server to negotiate one or more extensions, but the server didn't return them in the response message of the WebSocket handshake.


### -field WINHTTP_WEB_SOCKET_SERVER_ERROR_CLOSE_STATUS

An unexpected condition prevented the server from
      fulfilling the request.


### -field WINHTTP_WEB_SOCKET_SECURE_HANDSHAKE_ERROR_CLOSE_STATUS

The
      TLS handshake could not be completed.


#### - WINHTTP_WEB_SOCKET_INVALID_UTF8_CLOSE_STATUS

 UTF-8 frame carried an invalid UTF-8 stream.


## -remarks



<b>WINHTTP_WEB_SOCKET_CLOSE_STATUS</b> is used by <a href="https://docs.microsoft.com/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose">WinHttpWebSocketClose</a>, <a href="https://docs.microsoft.com/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketshutdown">WinHttpWebSocketShutdown</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketqueryclosestatus">WinHttpWebSocketQueryCloseStatus</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose">WinHttpWebSocketClose</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketqueryclosestatus">WinHttpWebSocketQueryCloseStatus</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketshutdown">WinHttpWebSocketShutdown</a>
 

 

