---
UID: NF:websocket.WebSocketReceive
title: WebSocketReceive function
author: windows-sdk-content
description: Adds a receive operation to the protocol component operation queue.
old-location: websock\websocketreceive.htm
tech.root: WebSock
ms.assetid: 6285c6fc-1f7a-45f3-ba28-94992e73693e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WebSocketReceive, WebSocketReceive function [Websocket Protocol Component API], websock.websocketreceive, websocket/WebSocketReceive
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Websocket.lib
req.dll: Websocket.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - websocket.dll
api_name:
 - WebSocketReceive
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WebSocketReceive function


## -description


The <b>WebSocketReceive</b> function adds a receive operation to the protocol component operation queue.


## -parameters




### -param hWebSocket [in]

Type: <b><a href="https://msdn.microsoft.com/D5D42785-CFAC-4324-9194-1BA8056FBAA1">WEB_SOCKET_HANDLE</a></b>

WebSocket session handle returned by a previous call to <a href="https://msdn.microsoft.com/c61992cc-7715-4fad-a66a-916402088ad0">WebSocketCreateClientHandle</a> or <a href="https://msdn.microsoft.com/f8c44a86-c586-48e3-b948-ed119bebf951">WebSocketCreateServerHandle</a>.


### -param pBuffer [in, optional]

Type: <b><a href="https://msdn.microsoft.com/05EC3940-4A17-4FBB-9446-15B511E18FF2">WEB_SOCKET_BUFFER</a>*</b>

A pointer to an array of <a href="https://msdn.microsoft.com/05EC3940-4A17-4FBB-9446-15B511E18FF2">WEB_SOCKET_BUFFER</a> structures that WebSocket data will be written to when it is returned by <a href="https://msdn.microsoft.com/566cff2d-15dd-45c6-bc41-550be1f45cfd">WebSocketGetAction</a>. If <b>NULL</b>, <b>WebSocketGetAction</b> will return an internal buffer that enables zero-copy scenarios.

<div class="alert"><b>Note</b>  Once <a href="https://msdn.microsoft.com/d9442e90-a74f-452d-b1b5-9f4285b39f10">WEB_SOCKET_INDICATE_RECEIVE_COMPLETE</a> is returned by <a href="https://msdn.microsoft.com/566cff2d-15dd-45c6-bc41-550be1f45cfd">WebSocketGetAction</a> for this action, the memory pointer to by <i>pBuffer</i> can be reclaimed.</div>
<div> </div>

### -param pvContext [in, optional]

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
 




## -see-also




<a href="https://msdn.microsoft.com/46d22fb5-adc3-4d1c-81b8-480f1c6de327">WEB_SOCKET_ACTION</a>



<a href="https://msdn.microsoft.com/fcfa67cf-9121-4f65-bba9-31ebca1291bd">WebSocketAbortHandle</a>



<a href="https://msdn.microsoft.com/e9b90176-c76f-42c2-b378-834a690bfe72">WebSocketCompleteAction</a>



<a href="https://msdn.microsoft.com/566cff2d-15dd-45c6-bc41-550be1f45cfd">WebSocketGetAction</a>



<a href="https://msdn.microsoft.com/289f3880-22ed-44f8-8a69-1c983153ea72">WebSocketSend</a>
 

 

