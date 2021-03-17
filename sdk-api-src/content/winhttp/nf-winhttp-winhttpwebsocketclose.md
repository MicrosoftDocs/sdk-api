---
UID: NF:winhttp.WinHttpWebSocketClose
title: WinHttpWebSocketClose function (winhttp.h)
description: Closes a WebSocket connection.
helpviewer_keywords: ["WinHttpWebSocketClose","WinHttpWebSocketClose function [WinHTTP]","http.winhttpwebsocketclose","winhttp/WinHttpWebSocketClose"]
old-location: http\winhttpwebsocketclose.htm
tech.root: http
ms.assetid: bbfde3db-d9a7-4fce-9d8b-6b57f9e432e1
ms.date: 12/05/2018
ms.keywords: WinHttpWebSocketClose, WinHttpWebSocketClose function [WinHTTP], http.winhttpwebsocketclose, winhttp/WinHttpWebSocketClose
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
 - WinHttpWebSocketClose
 - winhttp/WinHttpWebSocketClose
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
 - WinHttpWebSocketClose
---

# WinHttpWebSocketClose function


## -description

The <b>WinHttpWebSocketClose</b> function closes a WebSocket connection.

## -parameters

### -param hWebSocket [in]

Type: <b>HINTERNET</b>

Handle to a WebSocket.<div class="alert"><b>Note</b>  <b>WinHttpWebSocketClose</b> does not close this handle. To close the handle, call <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpclosehandle">WinHttpCloseHandle</a> on <i>hWebSocket</i> once it is no longer needed.</div>
<div> </div>

### -param usStatus [in]

Type: <b>USHORT</b>

A close status code. See <a href="/windows/desktop/api/winhttp/ne-winhttp-winhttp_web_socket_close_status">WINHTTP_WEB_SOCKET_CLOSE_STATUS</a> for possible values.

### -param pvReason [in, optional]

Type: <b>PVOID</b>

A detailed reason for the close.

### -param dwReasonLength [in]

Type: <b>DWORD</b>

The length of <i>pvReason</i>, in bytes.

If <i>pvReason</i> is NULL, this must be 0. This value must be within the range of 0 to 123.

## -returns

Type: <b>DWORD</b>

With the following exception, all error codes indicate that the underlying TCP connection has been aborted.

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
A close or send is pending.

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
</table>

## -remarks

<b>WinHttpWebSocketClose</b> completely closes a WebSocket connection. To close the send channel while still leaving the receive channel open, use <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketshutdown">WinHttpWebSocketShutdown</a>.

It is possible to  receive a close frame during regular receive operations. In this case, <b>WinHttpWebSocketClose</b> will also send a close frame.

The close timer can be set by the property
<a href="/windows/desktop/WinHttp/option-flags">WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT</a>.
The default is 10 seconds.

## -see-also

<a href="/windows/desktop/api/winhttp/ne-winhttp-winhttp_web_socket_close_status">WINHTTP_WEB_SOCKET_CLOSE_STATUS</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpclosehandle">WinHttpCloseHandle</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketshutdown">WinHttpWebSocketShutdown</a>