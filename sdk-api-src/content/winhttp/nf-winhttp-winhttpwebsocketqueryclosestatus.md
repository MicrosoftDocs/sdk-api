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
 

 

