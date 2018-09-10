---
UID: NF:winhttp.WinHttpWebSocketShutdown
title: WinHttpWebSocketShutdown function
author: windows-sdk-content
description: Sends a close frame to a WebSocket server to close the send channel, but leaves the receive channel open.
old-location: http\winhttpwebsocketshutdown.htm
tech.root: WinHttp
ms.assetid: C98FDBE1-DDBC-45c7-81FA-CB7C5940E3B5
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WinHttpWebSocketShutdown, WinHttpWebSocketShutdown function [WinHTTP], http.winhttpwebsocketshutdown, winhttp/WinHttpWebSocketShutdown
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
 - WinHttpWebSocketShutdown
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WinHttpWebSocketShutdown function


## -description


The <b>WinHttpWebSocketShutdown</b> function sends a close frame to a WebSocket server to close the send channel, but leaves the receive channel open.


## -parameters




### -param hWebSocket [in]

Type: <b>HINTERNET</b>

Handle to a WebSocket.<div class="alert"><b>Note</b>  <b>WinHttpWebSocketShutdown</b> does not close this handle. To close the handle, call <a href="https://msdn.microsoft.com/78215141-dfe8-4f0a-ba1a-a63fa257db6f">WinHttpCloseHandle</a> on <i>hWebSocket</i> once it is no longer needed.</div>
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
<dt><b>ERROR_IO_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The operation will complete asynchronously.

</td>
</tr>
</table>
 




## -remarks



<b>WinHttpWebSocketShutdown</b> sends a close frame and prevents additional data from being sent over the WebSocket connection. It does not close the receive channel. Use <a href="https://msdn.microsoft.com/bbfde3db-d9a7-4fce-9d8b-6b57f9e432e1">WinHttpWebSocketClose</a> when you want to completely close the connection and prevent any subsequent receive operations.

The application is responsible for receiving the close frame from the server (through regular receive operations).

After <b>WinHttpWebSocketShutdown</b> is called, the application can call <a href="https://msdn.microsoft.com/bbfde3db-d9a7-4fce-9d8b-6b57f9e432e1">WinHttpWebSocketClose</a> if it does not want to receive a close frame on its own and delegate it to the stack.




## -see-also




<a href="https://msdn.microsoft.com/d86795e4-3a30-4368-b253-1b126387efcc">WINHTTP_WEB_SOCKET_CLOSE_STATUS</a>



<a href="https://msdn.microsoft.com/78215141-dfe8-4f0a-ba1a-a63fa257db6f">WinHttpCloseHandle</a>



<a href="https://msdn.microsoft.com/bbfde3db-d9a7-4fce-9d8b-6b57f9e432e1">WinHttpWebSocketClose</a>
 

 

