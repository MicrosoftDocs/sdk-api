---
UID: NF:ws2spi.WPUResetEvent
title: WPUResetEvent function (ws2spi.h)
author: windows-sdk-content
description: The WPUResetEvent function resets the state of the specified event object to nonsignaled. This call is safe for use within interrupt context.
old-location: winsock\wpuresetevent_2.htm
tech.root: WinSock
ms.assetid: a3385c77-899c-4772-88b9-fb3e0fab54e0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WPUResetEvent, WPUResetEvent function [Winsock], _win32_wpuresetevent_2, winsock.wpuresetevent_2, ws2spi/WPUResetEvent
ms.topic: function
f1_keywords: ["ws2spi/WPUResetEvent"]
req.header: ws2spi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ws2spi.h
api_name:
 - WPUResetEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WPUResetEvent function


## -description


The 
<b>WPUResetEvent</b> function resets the state of the specified event object to nonsignaled. This call is safe for use within interrupt context.


## -parameters




### -param hEvent [in]

Handle that identifies an open event object.


### -param lpErrno [out]

Pointer to the error code.


## -returns



If no error occurs, the 
<b>WPUResetEvent</b> function returns the value <b>TRUE</b>. Otherwise, <b>FALSE</b> is returned, and a specific error code is available in <i>lpErrno</i>.



<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_INVALID_HANDLE</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>hEvent</i> parameter is not a valid event object handle.

</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wpucloseevent">WPUCloseEvent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wpucreateevent">WPUCreateEvent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wpusetevent">WPUSetEvent</a>
 

 

