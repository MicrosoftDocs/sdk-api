---
UID: NF:winhttp.WinHttpWebSocketReceive
title: WinHttpWebSocketReceive function (winhttp.h)
description: Receives data from a WebSocket connection.
helpviewer_keywords: ["WinHttpWebSocketReceive","WinHttpWebSocketReceive function [WinHTTP]","http.winhttpwebsocketreceive","winhttp/WinHttpWebSocketReceive"]
old-location: http\winhttpwebsocketreceive.htm
tech.root: http
ms.assetid: 9992150d-632b-45fe-8f11-84d698b4ffb3
ms.date: 12/05/2018
ms.keywords: WinHttpWebSocketReceive, WinHttpWebSocketReceive function [WinHTTP], http.winhttpwebsocketreceive, winhttp/WinHttpWebSocketReceive
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
req.lib: Winhttp.lib
req.dll: Winhttp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WinHttpWebSocketReceive
 - winhttp/WinHttpWebSocketReceive
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winhttp.dll
api_name:
 - WinHttpWebSocketReceive
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

Type: <b><a href="/windows/desktop/api/winhttp/ne-winhttp-winhttp_web_socket_buffer_type">WINHTTP_WEB_SOCKET_BUFFER_TYPE</a>*</b>

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
A close or receive is pending, or the receive channel has already been closed.

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
<dt><b>ERROR_WINHTTP_INVALID_SERVER_RESPONSE</b></dt>
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
The operation was cancelled because <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose">WinHttpWebSocketClose</a> was called to close the connection.

</td>
</tr>
</table>
