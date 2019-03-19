---
UID: NS:winhttp._WINHTTP_WEB_SOCKET_STATUS
title: WINHTTP_WEB_SOCKET_STATUS (winhttp.h)
author: windows-sdk-content
description: The WINHTTP_WEB_SOCKET_STATUS enumeration includes the status of a WebSocket operation.
old-location: http\winhttp_web_socket_status.htm
tech.root: WinHttp
ms.assetid: 4e34a306-1238-4a3b-8336-475e904b0a60
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WINHTTP_WEB_SOCKET_STATUS, WINHTTP_WEB_SOCKET_STATUS structure [HTTP], http.winhttp_web_socket_status, winhttp/WINHTTP_WEB_SOCKET_STATUS
ms.topic: struct
req.header: winhttp.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winhttp.h
api_name:
 - WINHTTP_WEB_SOCKET_STATUS
product: Windows
targetos: Windows
req.typenames: WINHTTP_WEB_SOCKET_STATUS
req.redist: 
---

# WINHTTP_WEB_SOCKET_STATUS structure


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
 

 

