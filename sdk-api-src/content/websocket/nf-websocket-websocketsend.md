---
UID: NF:websocket.WebSocketSend
title: WebSocketSend function
author: windows-sdk-content
description: Adds a send operation to the protocol component operation queue.
old-location: websock\websocketsend.htm
old-project: WebSock
ms.assetid: 289f3880-22ed-44f8-8a69-1c983153ea72
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: WebSocketSend, WebSocketSend function [Websocket Protocol Component API], websock.websocketsend, websocket/WebSocketSend
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
 - WebSocketSend
product: Windows
targetos: Windows
req.lib: Websocket.lib
req.dll: Websocket.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WebSocketSend function


## -description


The <b>WebSocketSend</b> function adds a send operation to the protocol component operation queue.


## -parameters




### -param hWebSocket [in]

Type: <b><a href="https://msdn.microsoft.com/D5D42785-CFAC-4324-9194-1BA8056FBAA1">WEB_SOCKET_HANDLE</a></b>

WebSocket session handle returned by a previous call to <a href="https://msdn.microsoft.com/c61992cc-7715-4fad-a66a-916402088ad0">WebSocketCreateClientHandle</a> or <a href="https://msdn.microsoft.com/f8c44a86-c586-48e3-b948-ed119bebf951">WebSocketCreateServerHandle</a>.


### -param BufferType [in]

Type: <b><a href="https://msdn.microsoft.com/a6657b51-ac16-4637-8dfd-e3dade951385">WEB_SOCKET_BUFFER_TYPE</a></b>

The type of WebSocket buffer data to send in <i>pBuffer</i>.


### -param pBuffer [in, optional]

Type: <b><a href="https://msdn.microsoft.com/05EC3940-4A17-4FBB-9446-15B511E18FF2">WEB_SOCKET_BUFFER</a>*</b>

A pointer to an array of <a href="https://msdn.microsoft.com/05EC3940-4A17-4FBB-9446-15B511E18FF2">WEB_SOCKET_BUFFER</a> structures that contains WebSocket buffer data to send. If <i>BufferType</i> is <a href="https://msdn.microsoft.com/a6657b51-ac16-4637-8dfd-e3dade951385">WEB_SOCKET_PING_PONG_BUFFER_TYPE</a> or <a href="https://msdn.microsoft.com/a6657b51-ac16-4637-8dfd-e3dade951385">WEB_SOCKET_UNSOLICITED_PONG_BUFFER_TYPE</a>, <i>pBuffer</i> must be <b>NULL</b>.

<div class="alert"><b>Note</b>  Once <a href="https://msdn.microsoft.com/d9442e90-a74f-452d-b1b5-9f4285b39f10">WEB_SOCKET_INDICATE_SEND_COMPLETE</a> is returned by <a href="https://msdn.microsoft.com/566cff2d-15dd-45c6-bc41-550be1f45cfd">WebSocketGetAction</a> for this action, the memory pointer to by <i>pBuffer</i> can be reclaimed.</div>
<div> </div>

### -param Context [in, optional]

Type: <b>PVOID</b>

A pointer to an application context handle that will be returned by a subsequent call to  <a href="https://msdn.microsoft.com/566cff2d-15dd-45c6-bc41-550be1f45cfd">WebSocketGetAction</a>.


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
<dt><b>E_INVALID_PROTOCOL_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
Protocol performed an invalid operation.

</td>
</tr>
</table>
 




## -remarks



After an application sends a <a href="https://msdn.microsoft.com/d9442e90-a74f-452d-b1b5-9f4285b39f10">WEB_SOCKET_CLOSE_BUFFER_TYPE</a> WebSocket buffer successfully, it can only send control frames.




## -see-also




<a href="https://msdn.microsoft.com/46d22fb5-adc3-4d1c-81b8-480f1c6de327">WEB_SOCKET_ACTION</a>



<a href="https://msdn.microsoft.com/fcfa67cf-9121-4f65-bba9-31ebca1291bd">WebSocketAbortHandle</a>



<a href="https://msdn.microsoft.com/e9b90176-c76f-42c2-b378-834a690bfe72">WebSocketCompleteAction</a>



<a href="https://msdn.microsoft.com/566cff2d-15dd-45c6-bc41-550be1f45cfd">WebSocketGetAction</a>



<a href="https://msdn.microsoft.com/6285c6fc-1f7a-45f3-ba28-94992e73693e">WebSocketReceive</a>
 

 

