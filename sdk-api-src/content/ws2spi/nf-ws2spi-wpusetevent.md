---
UID: NF:ws2spi.WPUSetEvent
title: WPUSetEvent function
author: windows-sdk-content
description: The WPUSetEvent function sets the state of the specified event object to signaled. This call is safe for use within interrupt context.
old-location: winsock\wpusetevent_2.htm
tech.root: WinSock
ms.assetid: d5caa926-1223-4917-85ba-4f79731e955a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WPUSetEvent, WPUSetEvent function [Winsock], _win32_wpusetevent_2, winsock.wpusetevent_2, ws2spi/WPUSetEvent
ms.topic: function
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
 - WPUSetEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WPUSetEvent function


## -description


The 
<b>WPUSetEvent</b> function sets the state of the specified event object to signaled. This call is safe for use within interrupt context.


## -parameters




### -param hEvent [in]

Handle that identifies an open event object.


### -param lpErrno [out]

Pointer to the error code.


## -returns



If no error occurs, the 
<b>WPUSetEvent</b> function returns the value <b>TRUE</b>. Otherwise, <b>FALSE</b> is returned, and a specific error code is available in <i>lpErrno</i>.



<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hEvent</i> parameter is not a valid event object handle.

</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/d8c6133b-e5a7-4936-a796-0930bb95fd0c">WPUCloseEvent</a>



<a href="https://msdn.microsoft.com/61e71e93-e35f-4122-bd4d-c103f652d2ca">WPUCreateEvent</a>



<a href="https://msdn.microsoft.com/a3385c77-899c-4772-88b9-fb3e0fab54e0">WPUResetEvent</a>
 

 

