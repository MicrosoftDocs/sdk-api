---
UID: NF:websocket.WebSocketBeginServerHandshake
title: WebSocketBeginServerHandshake function (websocket.h)
description: Begins the server-side handshake.
helpviewer_keywords: ["WebSocketBeginServerHandshake","WebSocketBeginServerHandshake function [Websocket Protocol Component API]","websock.websocketbeginserverhandshake","websocket/WebSocketBeginServerHandshake"]
old-location: websock\websocketbeginserverhandshake.htm
tech.root: WebSock
ms.assetid: 4009b56c-a92c-43fe-9e7b-2c38048aa748
ms.date: 12/05/2018
ms.keywords: WebSocketBeginServerHandshake, WebSocketBeginServerHandshake function [Websocket Protocol Component API], websock.websocketbeginserverhandshake, websocket/WebSocketBeginServerHandshake
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
 - WebSocketBeginServerHandshake
 - websocket/WebSocketBeginServerHandshake
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
 - WebSocketBeginServerHandshake
---

# WebSocketBeginServerHandshake function


## -description

The <b>WebSocketBeginServerHandshake</b> function  begins the server-side handshake.

## -parameters

### -param hWebSocket [in]

Type: <b><a href="/windows/desktop/WebSock/web-socket-protocol-component-api-data-types">WEB_SOCKET_HANDLE</a></b>

 WebSocket session handle returned by a previous call to <a href="/windows/desktop/api/websocket/nf-websocket-websocketcreateserverhandle">WebSocketCreateServerHandle</a>.

### -param pszSubprotocolSelected [in, optional]

Type: <b>PCSTR</b>

A pointer to a sub-protocol value chosen by the application. Must contain one subprotocol.

### -param pszExtensionSelected [in, optional]

Type: <b>PCSTR*</b>

A pointer to a list of extensions chosen by the application. Must contain one extension per entry.

### -param ulExtensionSelectedCount [in]

Type: <b>ULONG</b>

Number of extensions in <i>pszExtensionSelected</i>.

### -param pRequestHeaders [in]

Type: <b>const <a href="/windows/desktop/api/websocket/ns-websocket-web_socket_http_header">PWEB_SOCKET_HTTP_HEADER</a></b>

Pointer to an array of <a href="/windows/desktop/api/websocket/ns-websocket-web_socket_http_header">WEB_SOCKET_HTTP_HEADER</a> structures that contain the request headers received by the application.

### -param ulRequestHeaderCount [in]

Type: <b>ULONG</b>

Number of request headers in <i>pRequestHeaders</i>.

### -param pResponseHeaders [out]

Type: <b><a href="/windows/desktop/api/websocket/ns-websocket-web_socket_http_header">PWEB_SOCKET_HTTP_HEADER</a>*</b>

On successful output, a pointer to an array or <a href="/windows/desktop/api/websocket/ns-websocket-web_socket_http_header">WEB_SOCKET_HTTP_HEADER</a> structures that contain the response headers to be sent by the application.

### -param pulResponseHeaderCount [out]

Type: <b>ULONG*</b>

On successful output, number of response headers in <i>pResponseHeaders</i>.

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
</table>

## -remarks

To complete the server-side handshake, applications must call <a href="/windows/desktop/api/websocket/nf-websocket-websocketendserverhandshake">WebSocketEndServerHandshake</a> or any of the session functions. Once the client-server handshake is complete, the application may use the session functions.

## -see-also

<a href="/windows/desktop/api/websocket/ns-websocket-web_socket_http_header">WEB_SOCKET_HTTP_HEADER</a>



<a href="/windows/desktop/api/websocket/nf-websocket-websocketbeginclienthandshake">WebSocketBeginClientHandshake</a>



<a href="/windows/desktop/api/websocket/nf-websocket-websocketendclienthandshake">WebSocketEndClientHandshake</a>



<a href="/windows/desktop/api/websocket/nf-websocket-websocketendserverhandshake">WebSocketEndServerHandshake</a>