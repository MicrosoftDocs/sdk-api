---
UID: NF:websocket.WebSocketSend
title: WebSocketSend function (websocket.h)
description: Adds a send operation to the protocol component operation queue.
helpviewer_keywords: ["WebSocketSend","WebSocketSend function [Websocket Protocol Component API]","websock.websocketsend","websocket/WebSocketSend"]
old-location: websock\websocketsend.htm
tech.root: WebSock
ms.assetid: 289f3880-22ed-44f8-8a69-1c983153ea72
ms.date: 12/05/2018
ms.keywords: WebSocketSend, WebSocketSend function [Websocket Protocol Component API], websock.websocketsend, websocket/WebSocketSend
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
 - WebSocketSend
 - websocket/WebSocketSend
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
 - WebSocketSend
---

# WebSocketSend function


## -description

The <b>WebSocketSend</b> function adds a send operation to the protocol component operation queue.

## -parameters

### -param hWebSocket [in]

Type: <b><a href="/windows/desktop/WebSock/web-socket-protocol-component-api-data-types">WEB_SOCKET_HANDLE</a></b>

WebSocket session handle returned by a previous call to <a href="/windows/desktop/api/websocket/nf-websocket-websocketcreateclienthandle">WebSocketCreateClientHandle</a> or <a href="/windows/desktop/api/websocket/nf-websocket-websocketcreateserverhandle">WebSocketCreateServerHandle</a>.

### -param BufferType [in]

Type: <b><a href="/windows/desktop/api/websocket/ne-websocket-web_socket_buffer_type">WEB_SOCKET_BUFFER_TYPE</a></b>

The type of WebSocket buffer data to send in <i>pBuffer</i>.

### -param pBuffer [in, optional]

Type: <b><a href="/windows/desktop/api/websocket/ns-websocket-web_socket_buffer">WEB_SOCKET_BUFFER</a>*</b>

A pointer to an array of <a href="/windows/desktop/api/websocket/ns-websocket-web_socket_buffer">WEB_SOCKET_BUFFER</a> structures that contains WebSocket buffer data to send. If <i>BufferType</i> is <a href="/windows/desktop/api/websocket/ne-websocket-web_socket_buffer_type">WEB_SOCKET_PING_PONG_BUFFER_TYPE</a> or <a href="/windows/desktop/api/websocket/ne-websocket-web_socket_buffer_type">WEB_SOCKET_UNSOLICITED_PONG_BUFFER_TYPE</a>, <i>pBuffer</i> must be <b>NULL</b>.

<div class="alert"><b>Note</b>  Once <a href="/windows/desktop/api/websocket/ne-websocket-web_socket_property_type">WEB_SOCKET_INDICATE_SEND_COMPLETE</a> is returned by <a href="/windows/desktop/api/websocket/nf-websocket-websocketgetaction">WebSocketGetAction</a> for this action, the memory pointer to by <i>pBuffer</i> can be reclaimed.</div>
<div> </div>

### -param Context [in, optional]

Type: <b>PVOID</b>

A pointer to an application context handle that will be returned by a subsequent call to  <a href="/windows/desktop/api/websocket/nf-websocket-websocketgetaction">WebSocketGetAction</a>.

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
<dt><b>E_INVALID_PROTOCOL_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
Protocol performed an invalid operation.

</td>
</tr>
</table>

## -remarks

After an application sends a <a href="/windows/desktop/api/websocket/ne-websocket-web_socket_property_type">WEB_SOCKET_CLOSE_BUFFER_TYPE</a> WebSocket buffer successfully, it can only send control frames.

## -see-also

<a href="/windows/desktop/api/websocket/ne-websocket-web_socket_action">WEB_SOCKET_ACTION</a>



<a href="/windows/desktop/api/websocket/nf-websocket-websocketaborthandle">WebSocketAbortHandle</a>



<a href="/windows/desktop/api/websocket/nf-websocket-websocketcompleteaction">WebSocketCompleteAction</a>



<a href="/windows/desktop/api/websocket/nf-websocket-websocketgetaction">WebSocketGetAction</a>



<a href="/windows/desktop/api/websocket/nf-websocket-websocketreceive">WebSocketReceive</a>