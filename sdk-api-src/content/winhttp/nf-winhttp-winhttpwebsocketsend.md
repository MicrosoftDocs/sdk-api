---
UID: NF:winhttp.WinHttpWebSocketSend
title: WinHttpWebSocketSend function
author: windows-driver-content
description: Sends data over a WebSocket connection.
old-location: http\winhttpwebsocketsend.htm
old-project: WinHttp
ms.assetid: 24b45561-2a6e-4513-b597-15dbc10f0664
ms.author: windowsdriverdev
ms.date: 3/8/2018
ms.keywords: WinHttpWebSocketSend, WinHttpWebSocketSend function [WinHTTP], http.winhttpwebsocketsend, winhttp/WinHttpWebSocketSend
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: WINHTTP_WEB_SOCKET_OPERATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Winhttp.dll
api_name:
-	WinHttpWebSocketSend
product: Windows
targetos: Windows
req.lib: Winhttp.lib
req.dll: Winhttp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WinHttpWebSocketSend function


## -description


The <b>WinHttpWebSocketSend</b> function sends data over a WebSocket connection.


## -parameters




### -param hWebSocket [in]

Type: <b>HINTERNET</b>

Handle to a websocket.


### -param eBufferType [in]

Type: <b><a href="https://msdn.microsoft.com/9d730a6e-d05f-48ad-beec-cba6cc5cb17c">WINHTTP_WEB_SOCKET_BUFFER_TYPE</a></b>

Type of buffer.<div class="alert"><b>Note</b>  Do not specify <b>WINHTTP_WEB_SOCKET_CLOSE_BUFFER_TYPE</b>. Use <a href="https://msdn.microsoft.com/bbfde3db-d9a7-4fce-9d8b-6b57f9e432e1">WinHttpWebSocketClose</a> or <a href="https://msdn.microsoft.com/C98FDBE1-DDBC-45c7-81FA-CB7C5940E3B5">WinHttpWebSocketShutdown</a> to close the connection.</div>
<div> </div>



### -param pvBuffer [in]

Type: <b>PVOID</b>

Pointer to a buffer containing the data to send. Can be <b>NULL</b> only if <i>dwBufferLength</i> is 0.


### -param dwBufferLength [in]

Type: <b>DWORD</b>

Length of <i>pvBuffer</i>.


## -returns



Type: <b>DWORD</b>

<b>NO_ERROR</b> on success. Otherwise an error code.

<table>
<tr>
<th></th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
A close or send is pending, or the send channel has already been closed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/9d730a6e-d05f-48ad-beec-cba6cc5cb17c">WINHTTP_WEB_SOCKET_BUFFER_TYPE</a>
 

 

