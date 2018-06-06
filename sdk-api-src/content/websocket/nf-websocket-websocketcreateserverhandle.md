---
UID: NF:websocket.WebSocketCreateServerHandle
title: WebSocketCreateServerHandle function
author: windows-sdk-content
description: Creates a server-side WebSocket session handle.
old-location: websock\websocketcreateserverhandle.htm
old-project: WebSock
ms.assetid: f8c44a86-c586-48e3-b948-ed119bebf951
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: WebSocketCreateServerHandle, WebSocketCreateServerHandle function [Websocket Protocol Component API], websock.websocketcreateserverhandle, websocket/WebSocketCreateServerHandle
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
 - WebSocketCreateServerHandle
product: Windows
targetos: Windows
req.lib: Websocket.lib
req.dll: Websocket.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WebSocketCreateServerHandle function


## -description


The <b>WebSocketCreateServerHandle</b> function creates a server-side WebSocket session handle.


## -parameters




### -param pProperties [in]

Type: <b>const <a href="https://msdn.microsoft.com/c8b35288-4cc1-4839-a5be-4fd13b162c20">PWEB_SOCKET_PROPERTY</a></b>

Pointer to an array of <a href="https://msdn.microsoft.com/c8b35288-4cc1-4839-a5be-4fd13b162c20">WEB_SOCKET_PROPERTY</a> structures that contain WebSocket session-related properties.


### -param ulPropertyCount [in]

Type: <b>ULONG</b>

Number of properties in <i>pProperties</i>.


### -param phWebSocket [out]

Type: <b><a href="https://msdn.microsoft.com/D5D42785-CFAC-4324-9194-1BA8056FBAA1">WEB_SOCKET_HANDLE</a>*</b>

On successful output, pointer to a newly allocated server-side WebSocket session handle.


## -returns



Type: <b>HRESULT</b>

If the function succeeds, it returns <b>S_OK</b>.

If the function fails, it returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> defined in WinError.h.




## -see-also




<a href="https://msdn.microsoft.com/c8b35288-4cc1-4839-a5be-4fd13b162c20">WEB_SOCKET_PROPERTY</a>



<a href="https://msdn.microsoft.com/fcfa67cf-9121-4f65-bba9-31ebca1291bd">WebSocketAbortHandle</a>



<a href="https://msdn.microsoft.com/c61992cc-7715-4fad-a66a-916402088ad0">WebSocketCreateClientHandle</a>



<a href="https://msdn.microsoft.com/0ee21ee8-1375-4b42-8d04-64368e299b3e">WebSocketDeleteHandle</a>
 

 

