---
UID: NF:websocket.WebSocketAbortHandle
title: WebSocketAbortHandle function (websocket.h)
description: Aborts a WebSocket session handle created by WebSocketCreateClientHandle or WebSocketCreateServerHandle.
helpviewer_keywords: ["WebSocketAbortHandle","WebSocketAbortHandle function [Websocket Protocol Component API]","websock.websocketaborthandle","websocket/WebSocketAbortHandle"]
old-location: websock\websocketaborthandle.htm
tech.root: WebSock
ms.assetid: fcfa67cf-9121-4f65-bba9-31ebca1291bd
ms.date: 12/05/2018
ms.keywords: WebSocketAbortHandle, WebSocketAbortHandle function [Websocket Protocol Component API], websock.websocketaborthandle, websocket/WebSocketAbortHandle
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
 - WebSocketAbortHandle
 - websocket/WebSocketAbortHandle
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
 - WebSocketAbortHandle
---

# WebSocketAbortHandle function


## -description

The <b>WebSocketAbortHandle</b> function  aborts a WebSocket session handle created by <a href="/windows/desktop/api/websocket/nf-websocket-websocketcreateclienthandle">WebSocketCreateClientHandle</a> or <a href="/windows/desktop/api/websocket/nf-websocket-websocketcreateserverhandle">WebSocketCreateServerHandle</a>.

## -parameters

### -param hWebSocket [in]

Type: <b><a href="/windows/desktop/WebSock/web-socket-protocol-component-api-data-types">WEB_SOCKET_HANDLE</a></b>

 WebSocket session handle returned by a previous call to <a href="/windows/desktop/api/websocket/nf-websocket-websocketcreateclienthandle">WebSocketCreateClientHandle</a> or <a href="/windows/desktop/api/websocket/nf-websocket-websocketcreateserverhandle">WebSocketCreateServerHandle</a>.

## -returns

If the function succeeds, it returns <b>S_OK</b>.

If the function fails, it returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a> defined in WinError.h.

## -remarks

<b>WebSocketAbortHandle</b> aborts a <a href="/windows/desktop/WebSock/web-socket-protocol-component-api-data-types">WEB_SOCKET_HANDLE</a> session handle and any calls to <a href="/windows/desktop/api/websocket/nf-websocket-websocketsend">WebSocketSend</a> or <a href="/windows/desktop/api/websocket/nf-websocket-websocketreceive">WebSocketReceive</a> will return error when called with an aborted handle. <b>WebSocketAbortHandle</b> is a no-op if the WebSocket handshake has not been completed and the session handle has not been initialized. Any send/receive operations that were queued using <b>WebSocketSend</b> or <b>WebSocketReceive</b> will be ready to process using <a href="/windows/desktop/api/websocket/nf-websocket-websocketgetaction">WebSocketGetAction</a>, but attempts to queue additional operations using the aborted handle will result in error.

## -see-also

<a href="/windows/desktop/api/websocket/nf-websocket-websocketcreateclienthandle">WebSocketCreateClientHandle</a>



<a href="/windows/desktop/api/websocket/nf-websocket-websocketcreateserverhandle">WebSocketCreateServerHandle</a>



<a href="/windows/desktop/api/websocket/nf-websocket-websocketdeletehandle">WebSocketDeleteHandle</a>