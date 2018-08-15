---
UID: NF:winhttp.WinHttpWebSocketReceive
title: WinHttpWebSocketReceive function
author: windows-sdk-content
description: Receives data from a WebSocket connection.
old-location: http\winhttpwebsocketreceive.htm
old-project: winhttp
ms.assetid: 9992150d-632b-45fe-8f11-84d698b4ffb3
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WinHttpWebSocketReceive, WinHttpWebSocketReceive function [WinHTTP], http.winhttpwebsocketreceive, winhttp/WinHttpWebSocketReceive
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winhttp.h
req.include-header: 
req.redist: 
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
req.typenames: WINHTTP_WEB_SOCKET_OPERATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winhttp.dll
api_name:
 - WinHttpWebSocketReceive
product: Windows
targetos: Windows
req.lib: Winhttp.lib
req.dll: Winhttp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WinHttpWebSocketReceive function


## -description


The <b>WinHttpWebSocketReceive</b> function receives data from a WebSocket connection.


## -parameters




### -param hWebSocket [in]

Type: <b>HINTERNET</b>

Handle to a WebSocket.


### -param pvBuffer [out]

Type: <b>PVOID</b>

Pointer to a buffer to receive the data.


### -param dwBufferLength [in]

Type: <b>DWORD</b>

Length of <i>pvBuffer</i>, in bytes.


### -param pdwBytesRead [out]

Type: <b>DWORD*</b>

Pointer to a <b>DWORD</b> that receives the number of bytes read from the connection at the end of the operation. This is set only if <b>WinHttpWebSocketReceive</b> returns <b>NO_ERROR</b> and the handle was opened in synchronous mode.


### -param peBufferType [out]

Type: <b><a href="https://msdn.microsoft.com/9d730a6e-d05f-48ad-beec-cba6cc5cb17c">WINHTTP_WEB_SOCKET_BUFFER_TYPE</a>*</b>

The type of a returned buffer. This is only set if <b>WinHttpWebSocketReceive</b> returns <b>NO_ERROR</b> and the handle was opened in synchronous mode.


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
A close or send is pending, or the receive channel has already been closed.

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
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_SERVER_RESPONSE</b></dt>
</dl>
</td>
<td width="60%">
Invalid data was received from the server.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_OPERATION_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
The operation was cancelled because <a href="https://msdn.microsoft.com/bbfde3db-d9a7-4fce-9d8b-6b57f9e432e1">WinHttpWebSocketClose</a> was called to close the connection.

</td>
</tr>
</table>
 



