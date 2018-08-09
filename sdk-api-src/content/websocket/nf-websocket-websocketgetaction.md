---
UID: NF:websocket.WebSocketGetAction
title: WebSocketGetAction function
author: windows-sdk-content
description: Returns an action from a call to WebSocketSend, WebSocketReceive or WebSocketCompleteAction.
old-location: websock\websocketgetaction.htm
old-project: WebSock
ms.assetid: 566cff2d-15dd-45c6-bc41-550be1f45cfd
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: WebSocketGetAction, WebSocketGetAction function [Websocket Protocol Component API], websock.websocketgetaction, websocket/WebSocketGetAction
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: WEB_SOCKET_PROPERTY_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - websocket.dll
api_name:
 - WebSocketGetAction
product: Windows
targetos: Windows
req.lib: Websocket.lib
req.dll: Websocket.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WebSocketGetAction function


## -description


The <b>WebSocketGetAction</b> function returns an action from a call to <a href="https://msdn.microsoft.com/289f3880-22ed-44f8-8a69-1c983153ea72">WebSocketSend</a>, <a href="https://msdn.microsoft.com/6285c6fc-1f7a-45f3-ba28-94992e73693e">WebSocketReceive</a> or <a href="https://msdn.microsoft.com/e9b90176-c76f-42c2-b378-834a690bfe72">WebSocketCompleteAction</a>.


## -parameters




### -param hWebSocket [in]

Type: <b><a href="https://msdn.microsoft.com/D5D42785-CFAC-4324-9194-1BA8056FBAA1">WEB_SOCKET_HANDLE</a></b>

WebSocket session handle returned by a previous call to <a href="https://msdn.microsoft.com/c61992cc-7715-4fad-a66a-916402088ad0">WebSocketCreateClientHandle</a> or <a href="https://msdn.microsoft.com/f8c44a86-c586-48e3-b948-ed119bebf951">WebSocketCreateServerHandle</a>.


### -param eActionQueue [in]

Type: <b><a href="https://msdn.microsoft.com/59550c5a-a378-4162-a1cc-ed2d05662637">WEB_SOCKET_ACTION_QUEUE</a></b>

Enumeration that specifies whether to query the send queue, the receive queue, or both.


### -param pDataBuffers [in, out]

Type: <b><a href="https://msdn.microsoft.com/05EC3940-4A17-4FBB-9446-15B511E18FF2">WEB_SOCKET_BUFFER</a>*</b>

Pointer to an array of <a href="https://msdn.microsoft.com/05EC3940-4A17-4FBB-9446-15B511E18FF2">WEB_SOCKET_BUFFER</a> structures that contain WebSocket buffer data.

<div class="alert"><b>Note</b>  Do not allocate or deallocate memory for <a href="https://msdn.microsoft.com/05EC3940-4A17-4FBB-9446-15B511E18FF2">WEB_SOCKET_BUFFER</a> structures, because they will be overwritten by <b>WebSocketGetAction</b>. The memory for buffers returned by <b>WebSocketGetAction</b> are managed by the library.</div>
<div> </div>

### -param pulDataBufferCount [in, out]

Type: <b>ULONG*</b>

On input, pointer to a value that specifies the number of elements in <i>pDataBuffers</i>. On successful output, number of elements that were actually returned in <i>pDataBuffers</i>.


### -param pAction [out]

Type: <b><a href="https://msdn.microsoft.com/46d22fb5-adc3-4d1c-81b8-480f1c6de327">WEB_SOCKET_ACTION</a>*</b>

On successful output, pointer to a <a href="https://msdn.microsoft.com/46d22fb5-adc3-4d1c-81b8-480f1c6de327">WEB_SOCKET_ACTION</a> enumeration that specifies the action returned from the query to the queue defines in <i>eActionQueue</i>.


### -param pBufferType [out]

Type: <b><a href="https://msdn.microsoft.com/a6657b51-ac16-4637-8dfd-e3dade951385">WEB_SOCKET_BUFFER_TYPE</a>*</b>

On successful output, pointer to a <a href="https://msdn.microsoft.com/a6657b51-ac16-4637-8dfd-e3dade951385">WEB_SOCKET_BUFFER_TYPE</a> enumeration that specifies the type of Web Socket buffer data returned in <i>pDataBuffers</i>.


### -param pvApplicationContext [out, optional]

Type: <b>PVOID*</b>

On successful output, pointer to an application context handle. The context returned here was initially passed to <a href="https://msdn.microsoft.com/289f3880-22ed-44f8-8a69-1c983153ea72">WebSocketSend</a> or <a href="https://msdn.microsoft.com/6285c6fc-1f7a-45f3-ba28-94992e73693e">WebSocketReceive</a>. <i>pvApplicationContext</i> is not set if <i>pAction</i> is <a href="https://msdn.microsoft.com/46d22fb5-adc3-4d1c-81b8-480f1c6de327">WEB_SOCKET_NO_ACTION</a> or <a href="https://msdn.microsoft.com/46d22fb5-adc3-4d1c-81b8-480f1c6de327">WEB_SOCKET_SEND_TO_NETWORK_ACTION</a> when sending a pong in response to receiving a ping.


### -param pvActionContext [out]

Type: <b>PVOID*</b>

On successful output, pointer to an action context handle. This handle is passed into a subsequent call <a href="https://msdn.microsoft.com/e9b90176-c76f-42c2-b378-834a690bfe72">WebSocketCompleteAction</a>.


## -returns



Type: <b>HRESULT</b>

If the function succeeds, it returns <b>S_OK</b>.

If the function fails, it returns one of the following or a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> defined in WinError.h.

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



Each call to <b>WebSocketGetAction</b> must be paired with a call to <a href="https://msdn.microsoft.com/e9b90176-c76f-42c2-b378-834a690bfe72">WebSocketCompleteAction</a>.

If the <i>ulBytesTransferred</i> parameter of <a href="https://msdn.microsoft.com/e9b90176-c76f-42c2-b378-834a690bfe72">WebSocketCompleteAction</a> is different than the sum of all buffer lengths for the <a href="https://msdn.microsoft.com/46d22fb5-adc3-4d1c-81b8-480f1c6de327">WEB_SOCKET_SEND_TO_NETWORK_ACTION</a> action or is zero for the <b>WEB_SOCKET_RECEIVE_FROM_NETWORK_ACTION</b> action, the WebSocket application will not send or receive all of the data requested.

<b>WebSocketGetAction</b> will return in <i>pAction</i>:

<ul>
<li>
<a href="https://msdn.microsoft.com/46d22fb5-adc3-4d1c-81b8-480f1c6de327">WEB_SOCKET_INDICATE_SEND_COMPLETE_ACTION</a> once an operation queued by  <a href="https://msdn.microsoft.com/289f3880-22ed-44f8-8a69-1c983153ea72">WebSocketSend</a> is completed.</li>
<li>
<a href="https://msdn.microsoft.com/46d22fb5-adc3-4d1c-81b8-480f1c6de327">WEB_SOCKET_INDICATE_RECEIVE_COMPLETE_ACTION</a> once an operation queued by <a href="https://msdn.microsoft.com/6285c6fc-1f7a-45f3-ba28-94992e73693e">WebSocketReceive</a> is completed.</li>
</ul>
There may be only one outstanding send and receive operation at a time, so the next action will be returned once the previous one has been completed using <a href="https://msdn.microsoft.com/e9b90176-c76f-42c2-b378-834a690bfe72">WebSocketCompleteAction</a>.




## -see-also




<a href="https://msdn.microsoft.com/46d22fb5-adc3-4d1c-81b8-480f1c6de327">WEB_SOCKET_ACTION</a>



<a href="https://msdn.microsoft.com/59550c5a-a378-4162-a1cc-ed2d05662637">WEB_SOCKET_ACTION_QUEUE</a>



<a href="https://msdn.microsoft.com/a6657b51-ac16-4637-8dfd-e3dade951385">WEB_SOCKET_BUFFER_TYPE</a>



<a href="https://msdn.microsoft.com/e9b90176-c76f-42c2-b378-834a690bfe72">WebSocketCompleteAction</a>



<a href="https://msdn.microsoft.com/6285c6fc-1f7a-45f3-ba28-94992e73693e">WebSocketReceive</a>



<a href="https://msdn.microsoft.com/289f3880-22ed-44f8-8a69-1c983153ea72">WebSocketSend</a>
 

 

