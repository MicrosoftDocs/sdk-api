---
UID: NF:winhttp.WinHttpWebSocketQueryCloseStatus
title: WinHttpWebSocketQueryCloseStatus function (winhttp.h)
author: windows-sdk-content
description: Retrieves the close status sent by a server.
old-location: http\winhttpwebsocketqueryclosestatus.htm
tech.root: WinHttp
ms.assetid: 9b439be5-9f3f-43c7-8800-224b6750a6c1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WinHttpWebSocketQueryCloseStatus, WinHttpWebSocketQueryCloseStatus function [WinHTTP], http.winhttpwebsocketqueryclosestatus, winhttp/WinHttpWebSocketQueryCloseStatus
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
req.lib: Winhttp.lib
req.dll: Winhttp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winhttp.dll
api_name:
 - WinHttpWebSocketQueryCloseStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WinHttpWebSocketQueryCloseStatus function


## -description


The <b>WinHttpWebSocketQueryCloseStatus</b> function retrieves the close status sent by a server.


## -parameters




### -param hWebSocket [in]

Type: <b>HINTERNET</b>

Handle to a WebSocket


### -param pusStatus [out]

Type: <b>USHORT*</b>

A pointer to a close status code that will be filled upon return. See <a href="https://msdn.microsoft.com/d86795e4-3a30-4368-b253-1b126387efcc">WINHTTP_WEB_SOCKET_CLOSE_STATUS</a> for possible values.


### -param pvReason [out]

Type: <b>PVOID</b>

A pointer to a buffer that will receive a close reason on return.


### -param dwReasonLength [in]

Type: <b>DWORD</b>

The length of the <i>pvReason</i> buffer, in bytes.


### -param pdwReasonLengthConsumed [out]

Type: <b>DWORD*</b>

The number of bytes consumed. If <i>pvReason</i> is <b>NULL</b> and <i>dwReasonLength</i> is 0, <i>pdwReasonLengthConsumed</i> will contain the size of the buffer that needs to be allocated by the calling application.


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
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
There is not enough space in <i>pvReason</i> to write the whole close reason.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
No close frame has been received yet.

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
 




## -remarks



Call <b>WinHttpWebSocketQueryCloseStatus</b> only after <a href="https://msdn.microsoft.com/bbfde3db-d9a7-4fce-9d8b-6b57f9e432e1">WinHttpWebSocketClose</a> succeeds or if <a href="https://msdn.microsoft.com/9992150d-632b-45fe-8f11-84d698b4ffb3">WinHttpWebSocketReceive</a> returns <b>WINHTTP_WEB_SOCKET_CLOSE_BUFFER_TYPE</b>.

<i>pdwReasonLengthConsumed</i> will never be greater than 123, so allocating buffer with at least 123 will guarantee that <b>ERROR_INSUFFICIENT_BUFFER</b> will never be returned.




## -see-also




<a href="https://msdn.microsoft.com/d86795e4-3a30-4368-b253-1b126387efcc">WINHTTP_WEB_SOCKET_CLOSE_STATUS</a>



<a href="https://msdn.microsoft.com/bbfde3db-d9a7-4fce-9d8b-6b57f9e432e1">WinHttpWebSocketClose</a>



<a href="https://msdn.microsoft.com/9992150d-632b-45fe-8f11-84d698b4ffb3">WinHttpWebSocketReceive</a>
 

 

