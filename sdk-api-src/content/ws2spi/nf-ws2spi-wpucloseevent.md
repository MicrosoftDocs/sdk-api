---
UID: NF:ws2spi.WPUCloseEvent
title: WPUCloseEvent function
author: windows-sdk-content
description: The WPUCloseEvent function closes an open event object handle.
old-location: winsock\wpucloseevent_2.htm
tech.root: winsock
ms.assetid: d8c6133b-e5a7-4936-a796-0930bb95fd0c
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: WPUCloseEvent, WPUCloseEvent function [Winsock], _win32_wpucloseevent_2, winsock.wpucloseevent_2, ws2spi/WPUCloseEvent
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - WPUCloseEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- WPUCloseEvent
: 
---

# WPUCloseEvent function


## -description


The 
<b>WPUCloseEvent</b> function closes an open event object handle.


## -parameters




### -param hEvent [in]

Handle to an open event object.


### -param lpErrno [out]

Pointer to the error code.


## -returns



If the function succeeds, the return value is <b>TRUE</b>. Otherwise, the return value is <b>FALSE</b> and a specific error code is available in <i>lpErrno</i>.



<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSA_INVALID_HANDLE</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>hEvent</i> parameter is not a valid event object handle.

</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/61e71e93-e35f-4122-bd4d-c103f652d2ca">WPUCreateEvent</a>
 

 

