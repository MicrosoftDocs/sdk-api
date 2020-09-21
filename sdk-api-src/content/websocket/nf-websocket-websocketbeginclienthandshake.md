---
UID: NF:websocket.WebSocketBeginClientHandshake
title: WebSocketBeginClientHandshake function (websocket.h)
description: Begins the client-side handshake.
helpviewer_keywords: ["WebSocketBeginClientHandshake","WebSocketBeginClientHandshake function [Websocket Protocol Component API]","websock.websocketbeginclienthandshake","websocket/WebSocketBeginClientHandshake"]
old-location: websock\websocketbeginclienthandshake.htm
tech.root: WebSock
ms.assetid: b326d32d-7226-46cd-b15b-b5547d3ec8cb
ms.date: 12/05/2018
ms.keywords: WebSocketBeginClientHandshake, WebSocketBeginClientHandshake function [Websocket Protocol Component API], websock.websocketbeginclienthandshake, websocket/WebSocketBeginClientHandshake
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
 - WebSocketBeginClientHandshake
 - websocket/WebSocketBeginClientHandshake
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
 - WebSocketBeginClientHandshake
---

# WebSocketBeginClientHandshake function


## -description

The <b>WebSocketBeginClientHandshake</b> function  begins the client-side handshake.

## -parameters

### -param hWebSocket [in]

Type: <b><a href="/windows/desktop/WebSock/web-socket-protocol-component-api-data-types">WEB_SOCKET_HANDLE</a></b>

 WebSocket session handle returned by a previous call to <a href="/windows/desktop/api/websocket/nf-websocket-websocketcreateclienthandle">WebSocketCreateClientHandle</a>.

### -param pszSubprotocols [in, optional]

Type: <b>PCSTR*</b>

Pointer to an array of sub-protocols chosen by the application. Once the client-server handshake is complete, the application must use the sub-protocol returned by <a href="/windows/desktop/api/websocket/nf-websocket-websocketendclienthandshake">WebSocketEndClientHandshake</a>. Must contain one subprotocol per entry.

### -param ulSubprotocolCount [in]

Type: <b>ULONG</b>

Number of sub-protocols in <i>pszSubprotocols</i>.

### -param pszExtensions [in, optional]

Type: <b>PCSTR*</b>

Pointer to an array of extensions chosen by the application. Once the client-server handshake is complete, the application must use the extension returned by <a href="/windows/desktop/api/websocket/nf-websocket-websocketendclienthandshake">WebSocketEndClientHandshake</a>. Must contain one extension per entry.

### -param ulExtensionCount [in]

Type: <b>ULONG</b>

Number of extensions in <i>pszExtensions</i>.

### -param pInitialHeaders [in, optional]

Type: <b>const <a href="/windows/desktop/api/websocket/ns-websocket-web_socket_http_header">PWEB_SOCKET_HTTP_HEADER</a></b>

Pointer to an array of <a href="/windows/desktop/api/websocket/ns-websocket-web_socket_http_header">WEB_SOCKET_HTTP_HEADER</a> structures that contain the request headers to be sent by the application. The array must include the <i>Host HTTP</i> header as defined in <a href="http://tools.ietf.org/html/rfc2616">RFC 2616</a>.

### -param ulInitialHeaderCount [in]

Type: <b>ULONG</b>

Number of request headers in <i>pInitialHeaders</i>.

### -param pAdditionalHeaders [out]

Type: <b><a href="/windows/desktop/api/websocket/ns-websocket-web_socket_http_header">PWEB_SOCKET_HTTP_HEADER</a></b>

On successful output, pointer to an array of <a href="/windows/desktop/api/websocket/ns-websocket-web_socket_http_header">WEB_SOCKET_HTTP_HEADER</a> structures that contain the request headers to be sent by the application. If any of these headers were specified in <i>pInitialHeaders</i>, the header must be replaced.

### -param pulAdditionalHeaderCount [out]

Type: <b>ULONG*</b>

On successful output, number of response headers in <i>pAdditionalHeaders</i>.

## -returns

Type: <b>HRESULT</b>

If the function succeeds, it returns <b>S_OK</b>.

If the function fails, it returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a> defined in WinError.h.

## -remarks

To complete the client-side handshake, applications must call <a href="/windows/desktop/api/websocket/nf-websocket-websocketendclienthandshake">WebSocketEndClientHandshake</a>. Once the client-server handshake is complete, the application may use the session functions.

## -see-also

<a href="/windows/desktop/api/websocket/ns-websocket-web_socket_http_header">WEB_SOCKET_HTTP_HEADER</a>



<a href="/windows/desktop/api/websocket/nf-websocket-websocketbeginserverhandshake">WebSocketBeginServerHandshake</a>



<a href="/windows/desktop/api/websocket/nf-websocket-websocketendclienthandshake">WebSocketEndClientHandshake</a>



<a href="/windows/desktop/api/websocket/nf-websocket-websocketendserverhandshake">WebSocketEndServerHandshake</a>