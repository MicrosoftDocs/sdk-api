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

# WPUQueueApc function


## -description



			The 
<b>WPUQueueApc</b> function queues a user mode–asynchronous procedure call (APC) to the specified thread in order to facilitate invocation of overlapped I/O completion routines.


## -parameters




### -param lpThreadId [in]

Pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff565964">WSATHREADID</a> structure that identifies the thread context. A pointer to this structure is supplied to the service provider by the Ws2_32.dll as an input parameter to an overlapped operation. The provider should store the 
<b>WSATHREADID</b> structure locally and provide a pointer to this local store. The local copy of 
<b>WSATHREADID</b> is no longer needed once 
<b>WPUQueueApc</b> returns.


### -param lpfnUserApc [in]

Pointer to the APC function to be called.


### -param dwContext [in]

32-bit context value that is subsequently supplied as an input parameter to the APC function.


### -param lpErrno [out]

Pointer to the error code.


## -returns




						If no error occurs, 
<b>WPUQueueApc</b> returns zero and queues the completion routine for the specified thread. Otherwise, it returns SOCKET_ERROR, and a specific error code is available in <i>lpErrno</i>.



<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>dwThreadId</i> parameter does not specify a valid thread.

</td>
</tr>
</table>
 


<div> </div>





## -remarks



This function queues an APC function against the specified thread. Under Windows, this will be done using a user mode–asynchronous procedure call (APC). The APC will only execute when the specified thread is blocked in an alertable wait and a callback will be made directly. This call is safe for use within an interrupt context.

LPWSAUSERAPC is defined as follows:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>typedef void ( CALLBACK FAR * LPWSAUSERAPC )( DWORD dwContext );
</pre>
</td>
</tr>
</table></span></div>
Because the APC mechanism supports only a single  context value, <i>lpfnUserApc</i> itself cannot be the client specified–completion routine, which involves more parameters. The service provider must instead supply a pointer to its own APC function that uses the supplied <i>dwContext</i> value to access the needed result information for the overlapped operation, and then invokes the client specified–completion routine.

For service providers where a user-mode component implements overlapped I/O, a typical usage of the APC mechanism is as follows.

<ol>
<li>When the I/O operation completes, the provider allocates a small buffer and packs it with a pointer to the client-supplied completion procedure and parameter values to pass to the procedure.</li>
<li>It queues an APC, specifying the pointer to the buffer as the <i>dwContext</i> value and its own intermediate procedure as the target procedure <i>lpfnUserApc</i>.</li>
<li>When the target thread eventually enters alertable wait state, the service provider's intermediate procedure is called in the proper thread context.</li>
<li>The intermediate procedure simply unpacks parameters, deallocates the buffer, and calls the client-supplied completion procedure.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff565964">WSATHREADID</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566296">WSPIoctl</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566309">WSPRecv</a>



<a href="https://msdn.microsoft.com/f405cddf-b02e-41dd-bd65-fc73200c5fb3">WSPRecvFrom</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566316">WSPSend</a>



<a href="https://msdn.microsoft.com/9e788289-6545-4e5e-9d00-f284b2337fcd">WSPSendTo</a>
 

 

