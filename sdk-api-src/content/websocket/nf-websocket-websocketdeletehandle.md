---
UID: NF:websocket.WebSocketDeleteHandle
title: WebSocketDeleteHandle function
author: windows-sdk-content
description: Deletes a WebSocket session handle created by WebSocketCreateClientHandle or WebSocketCreateServerHandle.
old-location: websock\websocketdeletehandle.htm
old-project: WebSock
ms.assetid: 0ee21ee8-1375-4b42-8d04-64368e299b3e
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: WebSocketDeleteHandle, WebSocketDeleteHandle function [Websocket Protocol Component API], websock.websocketdeletehandle, websocket/WebSocketDeleteHandle
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
 - WebSocketDeleteHandle
product: Windows
targetos: Windows
req.lib: Websocket.lib
req.dll: Websocket.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WebSocketDeleteHandle function


## -description


The <b>WebSocketDeleteHandle</b> function deletes a WebSocket session handle created by <a href="https://msdn.microsoft.com/c61992cc-7715-4fad-a66a-916402088ad0">WebSocketCreateClientHandle</a> or <a href="https://msdn.microsoft.com/f8c44a86-c586-48e3-b948-ed119bebf951">WebSocketCreateServerHandle</a>.


## -parameters




### -param hWebSocket [in]

Type: <b><a href="https://msdn.microsoft.com/D5D42785-CFAC-4324-9194-1BA8056FBAA1">WEB_SOCKET_HANDLE</a></b>

WebSocket session handle returned by a previous call to <a href="https://msdn.microsoft.com/c61992cc-7715-4fad-a66a-916402088ad0">WebSocketCreateClientHandle</a> or <a href="https://msdn.microsoft.com/f8c44a86-c586-48e3-b948-ed119bebf951">WebSocketCreateServerHandle</a>.


## -returns



If the function succeeds, it returns <b>S_OK</b>.

If the function fails, it returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> defined in WinError.h.




## -remarks



Any use of a deleted <a href="https://msdn.microsoft.com/D5D42785-CFAC-4324-9194-1BA8056FBAA1">WEB_SOCKET_HANDLE</a> session handle may result in an access violation.

Before an application deletes a session handle, it must ensure that all operations have been processed. Applications may use <a href="https://msdn.microsoft.com/fcfa67cf-9121-4f65-bba9-31ebca1291bd">WebSocketAbortHandle</a> to abort any queued operations before calling <b>WebSocketDeleteHandle</b>.




## -see-also




<a href="https://msdn.microsoft.com/fcfa67cf-9121-4f65-bba9-31ebca1291bd">WebSocketAbortHandle</a>



<a href="https://msdn.microsoft.com/c61992cc-7715-4fad-a66a-916402088ad0">WebSocketCreateClientHandle</a>



<a href="https://msdn.microsoft.com/f8c44a86-c586-48e3-b948-ed119bebf951">WebSocketCreateServerHandle</a>
 

 

