---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

