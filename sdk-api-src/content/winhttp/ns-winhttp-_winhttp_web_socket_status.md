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

# _WINHTTP_WEB_SOCKET_STATUS structure


## -description


The <b>WINHTTP_WEB_SOCKET_STATUS</b> enumeration includes the status of a WebSocket operation.


## -struct-fields




### -field dwBytesTransferred

Type: <b>DWORD</b>

The amount of bytes transferred in the operation.


### -field eBufferType

Type: <b><a href="https://msdn.microsoft.com/9d730a6e-d05f-48ad-beec-cba6cc5cb17c">WINHTTP_WEB_SOCKET_BUFFER_TYPE</a></b>

The type of data in the buffer.


## -remarks



A <b>WINHTTP_WEB_SOCKET_STATUS</b> structure is passed to the completion callback of <a href="https://msdn.microsoft.com/24b45561-2a6e-4513-b597-15dbc10f0664">WinHttpWebSocketSend</a> when <i>dwInternetStatus</i>  is <b>WINHTTP_CALLBACK_STATUS_READ_COMPLETE</b>.

A <b>WINHTTP_WEB_SOCKET_STATUS</b> structure is passed to the completion callback of <a href="https://msdn.microsoft.com/9992150d-632b-45fe-8f11-84d698b4ffb3">WinHttpWebSocketReceive</a> when <i>dwInternetStatus</i>  is <b>WINHTTP_CALLBACK_STATUS_WRITE_COMPLETE</b>.

A <b>WINHTTP_WEB_SOCKET_STATUS</b> structure is passed to the completion callback of <a href="https://msdn.microsoft.com/bbfde3db-d9a7-4fce-9d8b-6b57f9e432e1">WinHttpWebSocketClose</a> when <i>dwInternetStatus</i>  is <b>WINHTTP_CALLBACK_STATUS_CLOSE_COMPLETE</b>.

A <b>WINHTTP_WEB_SOCKET_STATUS</b> structure is passed to the completion callback of <a href="https://msdn.microsoft.com/C98FDBE1-DDBC-45c7-81FA-CB7C5940E3B5">WinHttpWebSocketShutdown</a> when <i>dwInternetStatus</i>  is <b>WINHTTP_CALLBACK_STATUS_SHUTDOWN_COMPLETE</b>.




## -see-also




<a href="https://msdn.microsoft.com/4d828e41-9073-407a-aab5-531f1d6d6d02">WINHTTP_STATUS_CALLBACK</a>



<a href="https://msdn.microsoft.com/9d730a6e-d05f-48ad-beec-cba6cc5cb17c">WINHTTP_WEB_SOCKET_BUFFER_TYPE</a>



<a href="https://msdn.microsoft.com/bbfde3db-d9a7-4fce-9d8b-6b57f9e432e1">WinHttpWebSocketClose</a>



<a href="https://msdn.microsoft.com/9992150d-632b-45fe-8f11-84d698b4ffb3">WinHttpWebSocketReceive</a>



<a href="https://msdn.microsoft.com/24b45561-2a6e-4513-b597-15dbc10f0664">WinHttpWebSocketSend</a>



<a href="https://msdn.microsoft.com/C98FDBE1-DDBC-45c7-81FA-CB7C5940E3B5">WinHttpWebSocketShutdown</a>
 

 

