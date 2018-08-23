---
UID: NF:winhttp.WinHttpWebSocketClose
title: WinHttpWebSocketClose function
author: windows-sdk-content
description: Closes a WebSocket connection.
old-location: http\winhttpwebsocketclose.htm
old-project: winhttp
ms.assetid: bbfde3db-d9a7-4fce-9d8b-6b57f9e432e1
ms.author: windowssdkdev
ms.date: 08/17/2018
ms.keywords: WinHttpWebSocketClose, WinHttpWebSocketClose function [WinHTTP], http.winhttpwebsocketclose, winhttp/WinHttpWebSocketClose
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
 - WinHttpWebSocketClose
product: Windows
targetos: Windows
req.lib: Winhttp.lib
req.dll: Winhttp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WinHttpWebSocketClose function


## -description


The <b>WinHttpWebSocketClose</b> function closes a WebSocket connection.


## -parameters




### -param hWebSocket [in]

Type: <b>HINTERNET</b>

Handle to a WebSocket.<div class="alert"><b>Note</b>  <b>WinHttpWebSocketClose</b> does not close this handle. To close the handle, call <a href="https://msdn.microsoft.com/78215141-dfe8-4f0a-ba1a-a63fa257db6f">WinHttpCloseHandle</a> on <i>hWebSocket</i> once it is no longer needed.</div>
<div> </div>



### -param usStatus [in]

Type: <b>USHORT</b>

A close status code. See <a href="https://msdn.microsoft.com/d86795e4-3a30-4368-b253-1b126387efcc">WINHTTP_WEB_SOCKET_CLOSE_STATUS</a> for possible values.


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



<b>WinHttpWebSocketClose</b> completely closes a WebSocket connection. To close the send channel while still leaving the receive channel open, use <a href="https://msdn.microsoft.com/C98FDBE1-DDBC-45c7-81FA-CB7C5940E3B5">WinHttpWebSocketShutdown</a>.

It is possible to  receive a close frame during regular receive operations. In this case, <b>WinHttpWebSocketClose</b> will also send a close frame.

The close timer can be set by the property
<a href="https://msdn.microsoft.com/2d0441f4-ddba-4f2a-8861-8803cad6f1ac">WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT</a>.
The default is 10 seconds.




## -see-also




<a href="https://msdn.microsoft.com/d86795e4-3a30-4368-b253-1b126387efcc">WINHTTP_WEB_SOCKET_CLOSE_STATUS</a>



<a href="https://msdn.microsoft.com/78215141-dfe8-4f0a-ba1a-a63fa257db6f">WinHttpCloseHandle</a>



<a href="https://msdn.microsoft.com/C98FDBE1-DDBC-45c7-81FA-CB7C5940E3B5">WinHttpWebSocketShutdown</a>
 

 

