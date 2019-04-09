---
UID: NF:ws2spi.WPUCreateEvent
title: WPUCreateEvent function (ws2spi.h)
author: windows-sdk-content
description: The WPUCreateEvent function creates a new event object.
old-location: winsock\wpucreateevent_2.htm
tech.root: WinSock
ms.assetid: 61e71e93-e35f-4122-bd4d-c103f652d2ca
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WPUCreateEvent, WPUCreateEvent function [Winsock], _win32_wpucreateevent_2, winsock.wpucreateevent_2, ws2spi/WPUCreateEvent
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
 - WPUCreateEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WPUCreateEvent function


## -description


The 
<b>WPUCreateEvent</b> function creates a new event object.


## -parameters




### -param lpErrno [out]

Pointer to the error code.


## -returns



If no error occurs, 
<b>WPUCreateEvent</b> function returns the handle of the event object.

Otherwise, the return value is WSA_INVALID_EVENT and a specific error code is available in <i>lpErrno</i>.



<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSA_NOT_ENOUGH_MEMORY</a></b></dt>
</dl>
</td>
<td width="60%">
There is not enough free memory available to create the event object.

</td>
</tr>
</table>
 


<div> </div>





## -remarks



The event object created by this function is manually reset with an initial state of nonsignaled. If a Windows service provider requires auto reset events, it can call the Windows <a href="https://msdn.microsoft.com/1f6d946e-c74c-4599-ac3d-b709216a0900">CreateEvent</a> function directly.




## -see-also




<a href="https://msdn.microsoft.com/d8c6133b-e5a7-4936-a796-0930bb95fd0c">WPUCloseEvent</a>
 

 

