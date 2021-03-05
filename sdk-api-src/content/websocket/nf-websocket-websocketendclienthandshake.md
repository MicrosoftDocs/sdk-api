---
UID: NF:websocket.WebSocketEndClientHandshake
title: WebSocketEndClientHandshake function (websocket.h)
description: Completes the client-side handshake.
helpviewer_keywords: ["WebSocketEndClientHandshake","WebSocketEndClientHandshake function [Websocket Protocol Component API]","websock.websocketendclienthandshake","websocket/WebSocketEndClientHandshake"]
old-location: websock\websocketendclienthandshake.htm
tech.root: WebSock
ms.assetid: 07f2b2b8-1997-4ac7-b498-56d1e1fba9ef
ms.date: 12/05/2018
ms.keywords: WebSocketEndClientHandshake, WebSocketEndClientHandshake function [Websocket Protocol Component API], websock.websocketendclienthandshake, websocket/WebSocketEndClientHandshake
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
req.lib: Websocket.lib
req.dll: Websocket.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WebSocketEndClientHandshake
 - websocket/WebSocketEndClientHandshake
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - websocket.dll
api_name:
 - WebSocketEndClientHandshake
---

# WebSocketEndClientHandshake function


## -description

The <b>WebSocketEndClientHandshake</b> function completes the client-side handshake.

## -parameters

### -param hWebSocket [in]

Type: <b><a href="/windows/desktop/WebSock/web-socket-protocol-component-api-data-types">WEB_SOCKET_HANDLE</a></b>

 WebSocket session handle returned by a previous call to <a href="/windows/desktop/api/websocket/nf-websocket-websocketcreateclienthandle">WebSocketCreateClientHandle</a>.

### -param pResponseHeaders [in]

Type: <b>const <a href="/windows/desktop/api/websocket/ns-websocket-web_socket_http_header">PWEB_SOCKET_HTTP_HEADER</a></b>

Pointer to an array of <a href="/windows/desktop/api/websocket/ns-websocket-web_socket_http_header">WEB_SOCKET_HTTP_HEADER</a> structures that contain the response headers received by the application.

### -param ulReponseHeaderCount [in]

Type: <b>ULONG</b>

Number of response headers in <i>pResponseHeaders</i>.

### -param pulSelectedExtensions [in, out, optional]

Type: <b>ULONG*</b>

On input, pointer to an array allocated by the application. On successful output, pointer to an array of numbers that represent the extensions chosen by the server during the client-server handshake. These number are the zero-based indices into the extensions array passed to  <i>pszExtensions</i> in <a href="/windows/desktop/api/websocket/nf-websocket-websocketbeginclienthandshake">WebSocketBeginClientHandshake</a>.

### -param pulSelectedExtensionCount [in, out, optional]

Type: <b>ULONG*</b>

On input, number of extensions allocated in <i>pulSelectedExtensions</i>. This must be at least equal to the number passed to <i>ulExtensionCount</i> in <b>WebSocketEndClientHandshake</b>. On successful output, number of extensions returned in <i>pulSelectedExtensions</i>.

### -param pulSelectedSubprotocol [in, out, optional]

Type: <b>ULONG*</b>

On successful output, pointer to a number that represents the sub-protocol chosen by the server during the client-server handshake. This number is the zero-based index into the sub-protocols array passed to  <i>pszSubprotocols</i> in <a href="/windows/desktop/api/websocket/nf-websocket-websocketbeginclienthandshake">WebSocketBeginClientHandshake</a>.

## -returns

Type: <b>HRESULT</b>

If the function succeeds, it returns <b>S_OK</b>.

If the function fails, it returns one of the following or a <a href="/windows/desktop/Debug/system-error-codes">system error code</a> defined in WinError.h.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALID_PROTOCOL_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
Protocol data had an invalid format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNSUPPORTED_SUBPROTOCOL</b></dt>
</dl>
</td>
<td width="60%">
Server does not accept any of the sub-protocols specified by the application.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNSUPPORTED_EXTENSION</b></dt>
</dl>
</td>
<td width="60%">
Server does not accept extensions specified by the application.

</td>
</tr>
</table>

## -remarks

This function must be called to complete the client-side handshake after a previous call to <a href="/windows/desktop/api/websocket/nf-websocket-websocketbeginclienthandshake">WebSocketBeginClientHandshake</a>. Once the client-server handshake is complete, the application may use the session functions.

## -see-also

<a href="/windows/desktop/api/websocket/ns-websocket-web_socket_http_header">WEB_SOCKET_HTTP_HEADER</a>



<a href="/windows/desktop/api/websocket/nf-websocket-websocketbeginclienthandshake">WebSocketBeginClientHandshake</a>



<a href="/windows/desktop/api/websocket/nf-websocket-websocketbeginserverhandshake">WebSocketBeginServerHandshake</a>



<a href="/windows/desktop/api/websocket/nf-websocket-websocketendserverhandshake">WebSocketEndServerHandshake</a>
