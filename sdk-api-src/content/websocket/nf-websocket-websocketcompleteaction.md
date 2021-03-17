---
UID: NF:websocket.WebSocketCompleteAction
title: WebSocketCompleteAction function (websocket.h)
description: Completes an action started by WebSocketGetAction.
helpviewer_keywords: ["WebSocketCompleteAction","WebSocketCompleteAction function [Websocket Protocol Component API]","websock.websocketcompleteaction","websocket/WebSocketCompleteAction"]
old-location: websock\websocketcompleteaction.htm
tech.root: WebSock
ms.assetid: e9b90176-c76f-42c2-b378-834a690bfe72
ms.date: 12/05/2018
ms.keywords: WebSocketCompleteAction, WebSocketCompleteAction function [Websocket Protocol Component API], websock.websocketcompleteaction, websocket/WebSocketCompleteAction
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
 - WebSocketCompleteAction
 - websocket/WebSocketCompleteAction
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
 - WebSocketCompleteAction
---

# WebSocketCompleteAction function


## -description

The <b>WebSocketCompleteAction</b> function  completes an action started by <a href="/windows/desktop/api/websocket/nf-websocket-websocketgetaction">WebSocketGetAction</a>.

## -parameters

### -param hWebSocket [in]

Type: <b><a href="/windows/desktop/WebSock/web-socket-protocol-component-api-data-types">WEB_SOCKET_HANDLE</a></b>

WebSocket session handle returned by a previous call to <a href="/windows/desktop/api/websocket/nf-websocket-websocketcreateclienthandle">WebSocketCreateClientHandle</a> or <a href="/windows/desktop/api/websocket/nf-websocket-websocketcreateserverhandle">WebSocketCreateServerHandle</a>.

### -param pvActionContext [in]

Type: <b>PVOID</b>

Pointer to an action context handle that was returned by a previous call to <a href="/windows/desktop/api/websocket/nf-websocket-websocketgetaction">WebSocketGetAction</a>.

### -param ulBytesTransferred [in]

Type: <b>ULONG</b>

Number of bytes transferred for the <a href="/windows/desktop/api/websocket/ne-websocket-web_socket_action">WEB_SOCKET_SEND_TO_NETWORK_ACTION</a> or <b>WEB_SOCKET_RECEIVE_FROM_NETWORK_ACTION</b> actions. This value must be 0 for all other actions.

## -returns

If the function succeeds, it returns <b>S_OK</b>.

If the function fails, it returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a> defined in WinError.h.

## -remarks

Each call to <a href="/windows/desktop/api/websocket/nf-websocket-websocketgetaction">WebSocketGetAction</a> must be paired with a call to <b>WebSocketCompleteAction</b>. For the following network actions, I/O errors can occur:


<ul>
<li>
<a href="/windows/desktop/api/websocket/ne-websocket-web_socket_action">WEB_SOCKET_SEND_TO_NETWORK_ACTION</a>: if <i>ulBytesTransferred</i> is different than the sum all buffer lengths returned from <a href="/windows/desktop/api/websocket/nf-websocket-websocketgetaction">WebSocketGetAction</a> the current send action is canceled and the next call to <b>WebSocketGetAction</b> will return <b>WEB_SOCKET_INDICATE_SEND_COMPLETE_ACTION</b> even if not all buffers passed to <a href="/windows/desktop/api/websocket/nf-websocket-websocketsend">WebSocketSend</a> were processed.</li>
<li>
<a href="/windows/desktop/api/websocket/ne-websocket-web_socket_action">WEB_SOCKET_RECEIVE_FROM_NETWORK_ACTION</a>: if <i>ulBytesTransferred</i> is 0, the current receive action is canceled and the next call to <a href="/windows/desktop/api/websocket/nf-websocket-websocketgetaction">WebSocketGetAction</a> will return <b>WEB_SOCKET_INDICATE_RECEIVE_COMPLETE_ACTION</b> even if not all buffers passed to <a href="/windows/desktop/api/websocket/nf-websocket-websocketreceive">WebSocketReceive</a> were processed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/websocket/ne-websocket-web_socket_action">WEB_SOCKET_ACTION</a>



<a href="/windows/desktop/api/websocket/nf-websocket-websocketgetaction">WebSocketGetAction</a>