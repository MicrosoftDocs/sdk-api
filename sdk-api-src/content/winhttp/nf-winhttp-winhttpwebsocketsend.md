---
UID: NF:winhttp.WinHttpWebSocketSend
title: WinHttpWebSocketSend function (winhttp.h)
description: Sends data over a WebSocket connection.
helpviewer_keywords: ["WinHttpWebSocketSend","WinHttpWebSocketSend function [WinHTTP]","http.winhttpwebsocketsend","winhttp/WinHttpWebSocketSend"]
old-location: http\winhttpwebsocketsend.htm
tech.root: http
ms.assetid: 24b45561-2a6e-4513-b597-15dbc10f0664
ms.date: 12/05/2018
ms.keywords: WinHttpWebSocketSend, WinHttpWebSocketSend function [WinHTTP], http.winhttpwebsocketsend, winhttp/WinHttpWebSocketSend
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
 - WinHttpWebSocketSend
 - winhttp/WinHttpWebSocketSend
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
 - WinHttpWebSocketSend
---

# WinHttpWebSocketSend function


## -description

The <b>WinHttpWebSocketSend</b> function sends data over a WebSocket connection.

## -parameters

### -param hWebSocket [in]

Type: <b>HINTERNET</b>

Handle to a websocket.

### -param eBufferType [in]

Type: <b><a href="/windows/desktop/api/winhttp/ne-winhttp-winhttp_web_socket_buffer_type">WINHTTP_WEB_SOCKET_BUFFER_TYPE</a></b>

Type of buffer.<div class="alert"><b>Note</b>  Do not specify <b>WINHTTP_WEB_SOCKET_CLOSE_BUFFER_TYPE</b>. Use <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose">WinHttpWebSocketClose</a> or <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketshutdown">WinHttpWebSocketShutdown</a> to close the connection.</div>
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

<a href="/windows/desktop/api/winhttp/ne-winhttp-winhttp_web_socket_buffer_type">WINHTTP_WEB_SOCKET_BUFFER_TYPE</a>