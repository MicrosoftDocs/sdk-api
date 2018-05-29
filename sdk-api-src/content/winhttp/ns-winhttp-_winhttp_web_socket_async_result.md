---
UID: NS:winhttp._WINHTTP_WEB_SOCKET_ASYNC_RESULT
title: "_WINHTTP_WEB_SOCKET_ASYNC_RESULT"
author: windows-sdk-content
description: The WINHTTP_WEB_SOCKET_ASYNC_RESULT includes the result status of a WebSocket operation.
old-location: http\winhttp_web_socket_async_result.htm
old-project: WinHttp
ms.assetid: 90424980-9e30-465d-b948-820251c05357
ms.author: windowssdkdev
ms.date: 03/08/2018
ms.keywords: WINHTTP_WEB_SOCKET_ASYNC_RESULT, WINHTTP_WEB_SOCKET_ASYNC_RESULT structure [HTTP], _WINHTTP_WEB_SOCKET_ASYNC_RESULT, http.http_web_socket_async_result, http.winhttp_web_socket_async_result, winhttp/WINHTTP_WEB_SOCKET_ASYNC_RESULT
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: WINHTTP_WEB_SOCKET_ASYNC_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	winhttp.h
api_name:
-	WINHTTP_WEB_SOCKET_ASYNC_RESULT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

