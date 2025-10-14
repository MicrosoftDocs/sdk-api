---
UID: NS:websocket._WEB_SOCKET_BUFFER
title: WEB_SOCKET_BUFFER (websocket.h)
description: Contains data for a specific WebSocket action.
helpviewer_keywords: ["*PWEB_SOCKET_BUFFER","WEB_SOCKET_BUFFER","WEB_SOCKET_BUFFER union [Websocket Protocol Component API]","websock.web_socket_buffer","websocket/WEB_SOCKET_BUFFER"]
old-location: websock\web_socket_buffer.htm
tech.root: WebSock
ms.assetid: 05EC3940-4A17-4FBB-9446-15B511E18FF2
ms.date: 12/05/2018
ms.keywords: '*PWEB_SOCKET_BUFFER, WEB_SOCKET_BUFFER, WEB_SOCKET_BUFFER union [Websocket Protocol Component API], websock.web_socket_buffer, websocket/WEB_SOCKET_BUFFER'
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
req.typenames: WEB_SOCKET_BUFFER, *PWEB_SOCKET_BUFFER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WEB_SOCKET_BUFFER
 - websocket/_WEB_SOCKET_BUFFER
 - PWEB_SOCKET_BUFFER
 - websocket/PWEB_SOCKET_BUFFER
 - WEB_SOCKET_BUFFER
 - websocket/WEB_SOCKET_BUFFER
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
 - WEB_SOCKET_BUFFER
---

# WEB_SOCKET_BUFFER structure


## -description

The <b>WEB_SOCKET_BUFFER</b> structure contains data for a specific WebSocket action.

## -struct-fields

### -field Data

### -field Data.pbBuffer

Type: <b>PBYTE</b>

Pointer to the WebSocket buffer data.

### -field Data.ulBufferLength

Type: <b>ULONG</b>

Length, in bytes, of the buffer pointed to by <b>pbBuffer</b>.

### -field CloseStatus

### -field CloseStatus.pbReason

Type: <b>PBYTE</b>

A point to a UTF-8 string that represents the reason the connection is closed. If <b>ulReasonLength</b> is 0, this must be <b>NULL</b>.

### -field CloseStatus.ulReasonLength

Type: <b>ULONG</b>

Length, in bytes, of the buffer pointed to by <b>pbReason</b>. It cannot exceed <b>WEB_SOCKET_MAX_CLOSE_REASON_LENGTH</b> (123 bytes).

### -field CloseStatus.usStatus

Type: <b>USHORT</b>


<a href="/windows/desktop/api/websocket/ne-websocket-web_socket_close_status">WEB_SOCKET_CLOSE_STATUS</a> enumeration that specifies the WebSocket status.

## -remarks

Application must use the <b>Data</b> struct for all buffer types except <b>WEB_SOCKET_CLOSE_BUFFER_TYPE</b>. The <b>CloseStatus</b> struct is used for <b>WEB_SOCKET_CLOSE_BUFFER_TYPE</b>.

## -see-also

<a href="/windows/desktop/api/websocket/ne-websocket-web_socket_buffer_type">WEB_SOCKET_BUFFER_TYPE</a>



<a href="/windows/desktop/api/websocket/nf-websocket-websocketgetaction">WebSocketGetAction</a>



<a href="/windows/desktop/api/websocket/nf-websocket-websocketreceive">WebSocketReceive</a>



<a href="/windows/desktop/api/websocket/nf-websocket-websocketsend">WebSocketSend</a>