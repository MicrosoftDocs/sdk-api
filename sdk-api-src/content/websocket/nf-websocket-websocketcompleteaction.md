---
UID: NF:websocket.WebSocketCompleteAction
title: WebSocketCompleteAction function
author: windows-sdk-content
description: Completes an action started by WebSocketGetAction.
old-location: websock\websocketcompleteaction.htm
old-project: WebSock
ms.assetid: e9b90176-c76f-42c2-b378-834a690bfe72
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: WebSocketCompleteAction, WebSocketCompleteAction function [Websocket Protocol Component API], websock.websocketcompleteaction, websocket/WebSocketCompleteAction
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
req.typenames: WEB_SOCKET_PROPERTY_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	websocket.dll
api_name:
-	WebSocketCompleteAction
product: Windows
targetos: Windows
req.lib: Websocket.lib
req.dll: Websocket.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WebSocketCompleteAction function


## -description


The <b>WebSocketCompleteAction</b> function  completes an action started by <a href="https://msdn.microsoft.com/566cff2d-15dd-45c6-bc41-550be1f45cfd">WebSocketGetAction</a>.


## -parameters




### -param hWebSocket [in]

Type: <b><a href="https://msdn.microsoft.com/D5D42785-CFAC-4324-9194-1BA8056FBAA1">WEB_SOCKET_HANDLE</a></b>

WebSocket session handle returned by a previous call to <a href="https://msdn.microsoft.com/c61992cc-7715-4fad-a66a-916402088ad0">WebSocketCreateClientHandle</a> or <a href="https://msdn.microsoft.com/f8c44a86-c586-48e3-b948-ed119bebf951">WebSocketCreateServerHandle</a>.


### -param pvActionContext [in]

Type: <b>PVOID</b>

Pointer to an action context handle that was returned by a previous call to <a href="https://msdn.microsoft.com/566cff2d-15dd-45c6-bc41-550be1f45cfd">WebSocketGetAction</a>.


### -param ulBytesTransferred [in]

Type: <b>ULONG</b>

Number of bytes transferred for the <a href="https://msdn.microsoft.com/46d22fb5-adc3-4d1c-81b8-480f1c6de327">WEB_SOCKET_SEND_TO_NETWORK_ACTION</a> or <b>WEB_SOCKET_RECEIVE_FROM_NETWORK_ACTION</b> actions. This value must be 0 for all other actions.


## -returns



If the function succeeds, it returns <b>S_OK</b>.

If the function fails, it returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> defined in WinError.h.




## -remarks



Each call to <a href="https://msdn.microsoft.com/566cff2d-15dd-45c6-bc41-550be1f45cfd">WebSocketGetAction</a> must be paired with a call to <b>WebSocketCompleteAction</b>. For the following network actions, I/O errors can occur:


<ul>
<li>
<a href="https://msdn.microsoft.com/46d22fb5-adc3-4d1c-81b8-480f1c6de327">WEB_SOCKET_SEND_TO_NETWORK_ACTION</a>: if <i>ulBytesTransferred</i> is different than the sum all buffer lengths returned from <a href="https://msdn.microsoft.com/566cff2d-15dd-45c6-bc41-550be1f45cfd">WebSocketGetAction</a> the current send action is canceled and the next call to <b>WebSocketGetAction</b> will return <b>WEB_SOCKET_INDICATE_SEND_COMPLETE_ACTION</b> even if not all buffers passed to <a href="https://msdn.microsoft.com/289f3880-22ed-44f8-8a69-1c983153ea72">WebSocketSend</a> were processed.</li>
<li>
<a href="https://msdn.microsoft.com/46d22fb5-adc3-4d1c-81b8-480f1c6de327">WEB_SOCKET_RECEIVE_FROM_NETWORK_ACTION</a>: if <i>ulBytesTransferred</i> is 0, the current receive action is canceled and the next call to <a href="https://msdn.microsoft.com/566cff2d-15dd-45c6-bc41-550be1f45cfd">WebSocketGetAction</a> will return <b>WEB_SOCKET_INDICATE_RECEIVE_COMPLETE_ACTION</b> even if not all buffers passed to <a href="https://msdn.microsoft.com/6285c6fc-1f7a-45f3-ba28-94992e73693e">WebSocketReceive</a> were processed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/46d22fb5-adc3-4d1c-81b8-480f1c6de327">WEB_SOCKET_ACTION</a>



<a href="https://msdn.microsoft.com/566cff2d-15dd-45c6-bc41-550be1f45cfd">WebSocketGetAction</a>
 

 

