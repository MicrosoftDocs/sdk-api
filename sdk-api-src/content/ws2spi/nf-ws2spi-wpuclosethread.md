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

# WPUCloseThread function


## -description



			The 
<b>WPUCloseThread</b> function closes a thread opened with a call to 
<a href="https://msdn.microsoft.com/92d21f29-240f-407e-89a7-bbbb8f9bf0eb">WPUOpenCurrentThread</a>.


## -parameters




### -param lpThreadId [in]

Pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff565964">WSATHREADID</a> structure that identifies the thread context. This structure must have been initialized by a previous call to 
<a href="https://msdn.microsoft.com/92d21f29-240f-407e-89a7-bbbb8f9bf0eb">WPUOpenCurrentThread</a>.


### -param lpErrno [out]

Pointer to the error code.


## -returns




						If no error occurs, 
<a href="https://msdn.microsoft.com/92d21f29-240f-407e-89a7-bbbb8f9bf0eb">WPUOpenCurrentThread</a> returns zero. Otherwise, it returns SOCKET_ERROR, and a specific error code is available in <i>lpErrno</i>.



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
<b>WPUCloseThread</b> function is used in a layered service provider to deallocate the resources that were initiated in a call by the 
<a href="https://msdn.microsoft.com/92d21f29-240f-407e-89a7-bbbb8f9bf0eb">WPUOpenCurrentThread</a> function. The 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff565964">WSATHREADID</a> structure in the <i>lpThreadId</i> is the thread to deallocate.

Every call to 
<a href="https://msdn.microsoft.com/92d21f29-240f-407e-89a7-bbbb8f9bf0eb">WPUOpenCurrentThread</a> must have a call to 
<b>WPUCloseThread</b>. These two functions are used when the overlapped functions, such as 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff566316">WSPSend</a>, are called in a lower layer of the service provider than the current thread.




## -see-also




<a href="https://msdn.microsoft.com/92d21f29-240f-407e-89a7-bbbb8f9bf0eb">WPUOpenCurrentThread</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565964">WSATHREADID</a>
 

 

