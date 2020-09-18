---
UID: NF:websocket.WebSocketReceive
title: WebSocketReceive function (websocket.h)
description: Adds a receive operation to the protocol component operation queue.
helpviewer_keywords: ["WebSocketReceive","WebSocketReceive function [Websocket Protocol Component API]","websock.websocketreceive","websocket/WebSocketReceive"]
old-location: websock\websocketreceive.htm
tech.root: WebSock
ms.assetid: 6285c6fc-1f7a-45f3-ba28-94992e73693e
ms.date: 12/05/2018
ms.keywords: WebSocketReceive, WebSocketReceive function [Websocket Protocol Component API], websock.websocketreceive, websocket/WebSocketReceive
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
 - WebSocketReceive
 - websocket/WebSocketReceive
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
 - WebSocketReceive
---

# WebSocketReceive function


## -description

The <b>WebSocketReceive</b> function adds a receive operation to the protocol component operation queue.

## -parameters

### -param hWebSocket [in]

Type: <b><a href="/windows/desktop/WebSock/web-socket-protocol-component-api-data-types">WEB_SOCKET_HANDLE</a></b>

WebSocket session handle returned by a previous call to <a href="/windows/desktop/api/websocket/nf-websocket-websocketcreateclienthandle">WebSocketCreateClientHandle</a> or <a href="/windows/desktop/api/websocket/nf-websocket-websocketcreateserverhandle">WebSocketCreateServerHandle</a>.

### -param pBuffer [in, optional]

Type: <b><a href="/windows/desktop/api/websocket/ns-websocket-web_socket_buffer">WEB_SOCKET_BUFFER</a>*</b>

A pointer to an array of <a href="/windows/desktop/api/websocket/ns-websocket-web_socket_buffer">WEB_SOCKET_BUFFER</a> structures that WebSocket data will be written to when it is returned by <a href="/windows/desktop/api/websocket/nf-websocket-websocketgetaction">WebSocketGetAction</a>. If <b>NULL</b>, <b>WebSocketGetAction</b> will return an internal buffer that enables zero-copy scenarios.

<div class="alert"><b>Note</b>  Once <a href="/windows/desktop/api/websocket/ne-websocket-web_socket_property_type">WEB_SOCKET_INDICATE_RECEIVE_COMPLETE</a> is returned by <a href="/windows/desktop/api/websocket/nf-websocket-websocketgetaction">WebSocketGetAction</a> for this action, the memory pointer to by <i>pBuffer</i> can be reclaimed.</div>
<div> </div>

### -param pvContext [in, optional]

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

## -see-also

<a href="/windows/desktop/api/websocket/ne-websocket-web_socket_action">WEB_SOCKET_ACTION</a>



<a href="/windows/desktop/api/websocket/nf-websocket-websocketaborthandle">WebSocketAbortHandle</a>



<a href="/windows/desktop/api/websocket/nf-websocket-websocketcompleteaction">WebSocketCompleteAction</a>



<a href="/windows/desktop/api/websocket/nf-websocket-websocketgetaction">WebSocketGetAction</a>



<a href="/windows/desktop/api/websocket/nf-websocket-websocketsend">WebSocketSend</a>