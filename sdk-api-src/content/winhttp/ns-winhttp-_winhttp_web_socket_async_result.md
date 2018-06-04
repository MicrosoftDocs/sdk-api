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

# _WINHTTP_WEB_SOCKET_ASYNC_RESULT structure


## -description


 The <b>WINHTTP_WEB_SOCKET_ASYNC_RESULT</b> includes the result status of a WebSocket operation.


## -struct-fields




### -field AsyncResult

Type: <b><a href="https://msdn.microsoft.com/31544ef1-2532-4e44-8747-7a693cef9ccd">WINHTTP_ASYNC_RESULT</a></b>

The result of a WebSocket operation.


### -field Operation

Type: <b><a href="https://msdn.microsoft.com/0db68b44-dbf4-4aa2-9bb7-3a5502ef39e7">WINHTTP_WEB_SOCKET_OPERATION</a></b>

The type of WebSocket operation.


## -remarks



A <b>WINHTTP_WEB_SOCKET_ASYNC_RESULT</b> structure is passed to the completion callbacks of WebSocket functions such as <a href="https://msdn.microsoft.com/24b45561-2a6e-4513-b597-15dbc10f0664">WinHttpWebSocketSend</a>, <a href="https://msdn.microsoft.com/9992150d-632b-45fe-8f11-84d698b4ffb3">WinHttpWebSocketReceive</a>, and <a href="https://msdn.microsoft.com/bbfde3db-d9a7-4fce-9d8b-6b57f9e432e1">WinHttpWebSocketClose</a> when <i>dwInternetStatus</i> is <b>WINHTTP_CALLBACK_STATUS_REQUEST_ERROR</b>.




## -see-also




<a href="https://msdn.microsoft.com/31544ef1-2532-4e44-8747-7a693cef9ccd">WINHTTP_ASYNC_RESULT</a>



<a href="https://msdn.microsoft.com/0db68b44-dbf4-4aa2-9bb7-3a5502ef39e7">WINHTTP_WEB_SOCKET_OPERATION</a>



<a href="https://msdn.microsoft.com/bbfde3db-d9a7-4fce-9d8b-6b57f9e432e1">WinHttpWebSocketClose</a>



<a href="https://msdn.microsoft.com/9992150d-632b-45fe-8f11-84d698b4ffb3">WinHttpWebSocketReceive</a>



<a href="https://msdn.microsoft.com/24b45561-2a6e-4513-b597-15dbc10f0664">WinHttpWebSocketSend</a>



<a href="https://msdn.microsoft.com/C98FDBE1-DDBC-45c7-81FA-CB7C5940E3B5">WinHttpWebSocketShutdown</a>
 

 

