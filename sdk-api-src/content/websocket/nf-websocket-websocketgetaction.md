---
UID: NF:websocket.WebSocketGetAction
title: WebSocketGetAction function (websocket.h)
description: Returns an action from a call to WebSocketSend, WebSocketReceive or WebSocketCompleteAction.
helpviewer_keywords: ["WebSocketGetAction","WebSocketGetAction function [Websocket Protocol Component API]","websock.websocketgetaction","websocket/WebSocketGetAction"]
old-location: websock\websocketgetaction.htm
tech.root: WebSock
ms.assetid: 566cff2d-15dd-45c6-bc41-550be1f45cfd
ms.date: 12/05/2018
ms.keywords: WebSocketGetAction, WebSocketGetAction function [Websocket Protocol Component API], websock.websocketgetaction, websocket/WebSocketGetAction
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
 - WebSocketGetAction
 - websocket/WebSocketGetAction
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
 - WebSocketGetAction
---

# WebSocketGetAction function


## -description

The <b>WebSocketGetAction</b> function returns an action from a call to <a href="/windows/desktop/api/websocket/nf-websocket-websocketsend">WebSocketSend</a>, <a href="/windows/desktop/api/websocket/nf-websocket-websocketreceive">WebSocketReceive</a> or <a href="/windows/desktop/api/websocket/nf-websocket-websocketcompleteaction">WebSocketCompleteAction</a>.

## -parameters

### -param hWebSocket [in]

Type: <b><a href="/windows/desktop/WebSock/web-socket-protocol-component-api-data-types">WEB_SOCKET_HANDLE</a></b>

WebSocket session handle returned by a previous call to <a href="/windows/desktop/api/websocket/nf-websocket-websocketcreateclienthandle">WebSocketCreateClientHandle</a> or <a href="/windows/desktop/api/websocket/nf-websocket-websocketcreateserverhandle">WebSocketCreateServerHandle</a>.

### -param eActionQueue [in]

Type: <b><a href="/windows/desktop/api/websocket/ne-websocket-web_socket_action_queue">WEB_SOCKET_ACTION_QUEUE</a></b>

Enumeration that specifies whether to query the send queue, the receive queue, or both.

### -param pDataBuffers [in, out]

Type: <b><a href="/windows/desktop/api/websocket/ns-websocket-web_socket_buffer">WEB_SOCKET_BUFFER</a>*</b>

Pointer to an array of <a href="/windows/desktop/api/websocket/ns-websocket-web_socket_buffer">WEB_SOCKET_BUFFER</a> structures that contain WebSocket buffer data.

<div class="alert"><b>Note</b>  Do not allocate or deallocate memory for <a href="/windows/desktop/api/websocket/ns-websocket-web_socket_buffer">WEB_SOCKET_BUFFER</a> structures, because they will be overwritten by <b>WebSocketGetAction</b>. The memory for buffers returned by <b>WebSocketGetAction</b> are managed by the library.</div>
<div> </div>

### -param pulDataBufferCount [in, out]

Type: <b>ULONG*</b>

On input, pointer to a value that specifies the number of elements in <i>pDataBuffers</i>. On successful output, number of elements that were actually returned in <i>pDataBuffers</i>.

### -param pAction [out]

Type: <b><a href="/windows/desktop/api/websocket/ne-websocket-web_socket_action">WEB_SOCKET_ACTION</a>*</b>

On successful output, pointer to a <a href="/windows/desktop/api/websocket/ne-websocket-web_socket_action">WEB_SOCKET_ACTION</a> enumeration that specifies the action returned from the query to the queue defines in <i>eActionQueue</i>.

### -param pBufferType [out]

Type: <b><a href="/windows/desktop/api/websocket/ne-websocket-web_socket_buffer_type">WEB_SOCKET_BUFFER_TYPE</a>*</b>

On successful output, pointer to a <a href="/windows/desktop/api/websocket/ne-websocket-web_socket_buffer_type">WEB_SOCKET_BUFFER_TYPE</a> enumeration that specifies the type of Web Socket buffer data returned in <i>pDataBuffers</i>.

### -param pvApplicationContext [out, optional]

Type: <b>PVOID*</b>

On successful output, pointer to an application context handle. The context returned here was initially passed to <a href="/windows/desktop/api/websocket/nf-websocket-websocketsend">WebSocketSend</a> or <a href="/windows/desktop/api/websocket/nf-websocket-websocketreceive">WebSocketReceive</a>. <i>pvApplicationContext</i> is not set if <i>pAction</i> is <a href="/windows/desktop/api/websocket/ne-websocket-web_socket_action">WEB_SOCKET_NO_ACTION</a> or <a href="/windows/desktop/api/websocket/ne-websocket-web_socket_action">WEB_SOCKET_SEND_TO_NETWORK_ACTION</a> when sending a pong in response to receiving a ping.

### -param pvActionContext [out]

Type: <b>PVOID*</b>

On successful output, pointer to an action context handle. This handle is passed into a subsequent call <a href="/windows/desktop/api/websocket/nf-websocket-websocketcompleteaction">WebSocketCompleteAction</a>.

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
 Protocol data had invalid format. This is only returned for receive operations.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALID_PROTOCOL_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
Protocol performed invalid operations. This is only returned for receive operations.

</td>
</tr>
</table>

## -remarks

Each call to <b>WebSocketGetAction</b> must be paired with a call to <a href="/windows/desktop/api/websocket/nf-websocket-websocketcompleteaction">WebSocketCompleteAction</a>.

If the <i>ulBytesTransferred</i> parameter of <a href="/windows/desktop/api/websocket/nf-websocket-websocketcompleteaction">WebSocketCompleteAction</a> is different than the sum of all buffer lengths for the <a href="/windows/desktop/api/websocket/ne-websocket-web_socket_action">WEB_SOCKET_SEND_TO_NETWORK_ACTION</a> action or is zero for the <b>WEB_SOCKET_RECEIVE_FROM_NETWORK_ACTION</b> action, the WebSocket application will not send or receive all of the data requested.

<b>WebSocketGetAction</b> will return in <i>pAction</i>:

<ul>
<li>
<a href="/windows/desktop/api/websocket/ne-websocket-web_socket_action">WEB_SOCKET_INDICATE_SEND_COMPLETE_ACTION</a> once an operation queued by  <a href="/windows/desktop/api/websocket/nf-websocket-websocketsend">WebSocketSend</a> is completed.</li>
<li>
<a href="/windows/desktop/api/websocket/ne-websocket-web_socket_action">WEB_SOCKET_INDICATE_RECEIVE_COMPLETE_ACTION</a> once an operation queued by <a href="/windows/desktop/api/websocket/nf-websocket-websocketreceive">WebSocketReceive</a> is completed.</li>
</ul>
There may be only one outstanding send and receive operation at a time, so the next action will be returned once the previous one has been completed using <a href="/windows/desktop/api/websocket/nf-websocket-websocketcompleteaction">WebSocketCompleteAction</a>.

## -see-also

<a href="/windows/desktop/api/websocket/ne-websocket-web_socket_action">WEB_SOCKET_ACTION</a>



<a href="/windows/desktop/api/websocket/ne-websocket-web_socket_action_queue">WEB_SOCKET_ACTION_QUEUE</a>



<a href="/windows/desktop/api/websocket/ne-websocket-web_socket_buffer_type">WEB_SOCKET_BUFFER_TYPE</a>



<a href="/windows/desktop/api/websocket/nf-websocket-websocketcompleteaction">WebSocketCompleteAction</a>



<a href="/windows/desktop/api/websocket/nf-websocket-websocketreceive">WebSocketReceive</a>



<a href="/windows/desktop/api/websocket/nf-websocket-websocketsend">WebSocketSend</a>