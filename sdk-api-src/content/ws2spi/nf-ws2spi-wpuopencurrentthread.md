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

# WPUOpenCurrentThread function


## -description



			The 
<b>WPUOpenCurrentThread</b> function opens a handle to the current thread that can be used with overlapped functions in a layered service provider. This is intended to be used by layered service providers that wish to initiate overlapped I/O from nonapplication threads.


## -parameters




### -param lpThreadId [out]

Pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff565964">WSATHREADID</a> structure that can then be passed to an overlapped function.


### -param lpErrno [out]

Pointer to the error code.


## -returns




						If no error occurs, 
<b>WPUOpenCurrentThread</b> returns the zero. Otherwise, it returns SOCKET_ERROR, and a specific error code is available in <i>lpErrno</i>.



<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSANOTINITIALISED</a></b></dt>
</dl>
</td>
<td width="60%">
A successful 
<a href="https://msdn.microsoft.com/9ebfe81c-bed6-4bde-b1dd-5eaefbaac9cf">WSPStartup</a> call must occur before using this function.

</td>
</tr>
</table>
 


<div> </div>





## -remarks



The 
<b>WPUOpenCurrentThread</b> function provides a pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff565964">WSATHREADID</a> structure that can then be passed to an overlapped function such as 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff566316">WSPSend</a> or 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff566309">WSPRecv</a>. Layered service providers using a private thread in one of the upper layers will use 
<b>WPUOpenCurrentThread</b> to pass a 
<b>WSATHREADID</b> pointer to the lower layer that is administering overlapped functions.

Overlapped functions such as 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff566316">WSPSend</a> and 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff566309">WSPRecv</a> can then be used in the same way as a regular service provider.

Every call to 
<b>WPUOpenCurrentThread</b> must have a corresponding call to 
<a href="https://msdn.microsoft.com/1a5e7a99-484f-4862-bd28-edf85debc8e5">WPUCloseThread</a>.




## -see-also




<a href="https://msdn.microsoft.com/1a5e7a99-484f-4862-bd28-edf85debc8e5">WPUCloseThread</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566309">WSPRecv</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566316">WSPSend</a>
 

 

