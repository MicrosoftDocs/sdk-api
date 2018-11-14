---
UID: NF:ws2spi.WPUCloseThread
title: WPUCloseThread function
author: windows-sdk-content
description: The WPUCloseThread function closes a thread opened with a call to WPUOpenCurrentThread.
old-location: winsock\wpuclosethread_2.htm
tech.root: winsock
ms.assetid: 1a5e7a99-484f-4862-bd28-edf85debc8e5
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: WPUCloseThread, WPUCloseThread function [Winsock], _win32_wpuclosethread_2, winsock.wpuclosethread_2, ws2spi/WPUCloseThread
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
 - WPUCloseThread
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- WPUCloseThread
: 
---

# WPUCloseThread function


## -description


The 
<b>WPUCloseThread</b> function closes a thread opened with a call to 
<a href="https://msdn.microsoft.com/92d21f29-240f-407e-89a7-bbbb8f9bf0eb">WPUOpenCurrentThread</a>.


## -parameters




### -param lpThreadId [in]

Pointer to a 
<a href="https://msdn.microsoft.com/eeea1139-1d14-4f53-bd64-833539b53bed">WSATHREADID</a> structure that identifies the thread context. This structure must have been initialized by a previous call to 
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
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSANOTINITIALISED</a></b></dt>
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
<a href="https://msdn.microsoft.com/eeea1139-1d14-4f53-bd64-833539b53bed">WSATHREADID</a> structure in the <i>lpThreadId</i> is the thread to deallocate.

Every call to 
<a href="https://msdn.microsoft.com/92d21f29-240f-407e-89a7-bbbb8f9bf0eb">WPUOpenCurrentThread</a> must have a call to 
<b>WPUCloseThread</b>. These two functions are used when the overlapped functions, such as 
<a href="https://msdn.microsoft.com/4d741663-34f5-41b9-ba8f-77d45382d50b">WSPSend</a>, are called in a lower layer of the service provider than the current thread.




## -see-also




<a href="https://msdn.microsoft.com/92d21f29-240f-407e-89a7-bbbb8f9bf0eb">WPUOpenCurrentThread</a>



<a href="https://msdn.microsoft.com/eeea1139-1d14-4f53-bd64-833539b53bed">WSATHREADID</a>
 

 

