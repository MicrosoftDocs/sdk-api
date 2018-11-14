---
UID: NF:websocket.WebSocketAbortHandle
title: WebSocketAbortHandle function
author: windows-sdk-content
description: Aborts a WebSocket session handle created by WebSocketCreateClientHandle or WebSocketCreateServerHandle.
old-location: websock\websocketaborthandle.htm
tech.root: WebSock
ms.assetid: fcfa67cf-9121-4f65-bba9-31ebca1291bd
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WebSocketAbortHandle, WebSocketAbortHandle function [Websocket Protocol Component API], websock.websocketaborthandle, websocket/WebSocketAbortHandle
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
 - WebSocketAbortHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- WebSocketAbortHandle
: 
---

# WebSocketAbortHandle function


## -description


The <b>WebSocketAbortHandle</b> function  aborts a WebSocket session handle created by <a href="https://msdn.microsoft.com/c61992cc-7715-4fad-a66a-916402088ad0">WebSocketCreateClientHandle</a> or <a href="https://msdn.microsoft.com/f8c44a86-c586-48e3-b948-ed119bebf951">WebSocketCreateServerHandle</a>.


## -parameters




### -param hWebSocket [in]

Type: <b><a href="https://msdn.microsoft.com/D5D42785-CFAC-4324-9194-1BA8056FBAA1">WEB_SOCKET_HANDLE</a></b>

 WebSocket session handle returned by a previous call to <a href="https://msdn.microsoft.com/c61992cc-7715-4fad-a66a-916402088ad0">WebSocketCreateClientHandle</a> or <a href="https://msdn.microsoft.com/f8c44a86-c586-48e3-b948-ed119bebf951">WebSocketCreateServerHandle</a>.


## -returns



If the function succeeds, it returns <b>S_OK</b>.

If the function fails, it returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> defined in WinError.h.




## -remarks



<b>WebSocketAbortHandle</b> aborts a <a href="https://msdn.microsoft.com/D5D42785-CFAC-4324-9194-1BA8056FBAA1">WEB_SOCKET_HANDLE</a> session handle and any calls to <a href="https://msdn.microsoft.com/289f3880-22ed-44f8-8a69-1c983153ea72">WebSocketSend</a> or <a href="https://msdn.microsoft.com/6285c6fc-1f7a-45f3-ba28-94992e73693e">WebSocketReceive</a> will return error when called with an aborted handle. <b>WebSocketAbortHandle</b> is a no-op if the WebSocket handshake has not been completed and the session handle has not been initialized. Any send/receive operations that were queued using <b>WebSocketSend</b> or <b>WebSocketReceive</b> will be ready to process using <a href="https://msdn.microsoft.com/566cff2d-15dd-45c6-bc41-550be1f45cfd">WebSocketGetAction</a>, but attempts to queue additional operations using the aborted handle will result in error.




## -see-also




<a href="https://msdn.microsoft.com/c61992cc-7715-4fad-a66a-916402088ad0">WebSocketCreateClientHandle</a>



<a href="https://msdn.microsoft.com/f8c44a86-c586-48e3-b948-ed119bebf951">WebSocketCreateServerHandle</a>



<a href="https://msdn.microsoft.com/0ee21ee8-1375-4b42-8d04-64368e299b3e">WebSocketDeleteHandle</a>
 

 

