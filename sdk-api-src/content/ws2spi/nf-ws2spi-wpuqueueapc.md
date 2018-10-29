---
UID: NF:ws2spi.WPUQueueApc
title: WPUQueueApc function
author: windows-sdk-content
description: The WPUQueueApc function queues a user mode&#8211;asynchronous procedure call (APC) to the specified thread in order to facilitate invocation of overlapped I/O completion routines.
old-location: winsock\wpuqueueapc_2.htm
tech.root: WinSock
ms.assetid: 4326547e-85e2-409c-9f36-aa013853dfd9
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: WPUQueueApc, WPUQueueApc function [Winsock], _win32_wpuqueueapc_2, winsock.wpuqueueapc_2, ws2spi/WPUQueueApc
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
 - WPUQueueApc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WPUQueueApc function


## -description


The 
<b>WPUQueueApc</b> function queues a user mode–asynchronous procedure call (APC) to the specified thread in order to facilitate invocation of overlapped I/O completion routines.


## -parameters




### -param lpThreadId [in]

Pointer to a 
<a href="https://msdn.microsoft.com/eeea1139-1d14-4f53-bd64-833539b53bed">WSATHREADID</a> structure that identifies the thread context. A pointer to this structure is supplied to the service provider by the Ws2_32.dll as an input parameter to an overlapped operation. The provider should store the 
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
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEFAULT</a></b></dt>
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


```cpp
typedef void ( CALLBACK FAR * LPWSAUSERAPC )( DWORD dwContext );

```


Because the APC mechanism supports only a single  context value, <i>lpfnUserApc</i> itself cannot be the client specified–completion routine, which involves more parameters. The service provider must instead supply a pointer to its own APC function that uses the supplied <i>dwContext</i> value to access the needed result information for the overlapped operation, and then invokes the client specified–completion routine.

For service providers where a user-mode component implements overlapped I/O, a typical usage of the APC mechanism is as follows.

<ol>
<li>When the I/O operation completes, the provider allocates a small buffer and packs it with a pointer to the client-supplied completion procedure and parameter values to pass to the procedure.</li>
<li>It queues an APC, specifying the pointer to the buffer as the <i>dwContext</i> value and its own intermediate procedure as the target procedure <i>lpfnUserApc</i>.</li>
<li>When the target thread eventually enters alertable wait state, the service provider's intermediate procedure is called in the proper thread context.</li>
<li>The intermediate procedure simply unpacks parameters, deallocates the buffer, and calls the client-supplied completion procedure.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/eeea1139-1d14-4f53-bd64-833539b53bed">WSATHREADID</a>



<a href="https://msdn.microsoft.com/098d85e3-8fe2-46c2-966d-deae4b12afd6">WSPIoctl</a>



<a href="https://msdn.microsoft.com/5304a5d6-bc99-4a6f-8eeb-668bbd93fc84">WSPRecv</a>



<a href="https://msdn.microsoft.com/f405cddf-b02e-41dd-bd65-fc73200c5fb3">WSPRecvFrom</a>



<a href="https://msdn.microsoft.com/4d741663-34f5-41b9-ba8f-77d45382d50b">WSPSend</a>



<a href="https://msdn.microsoft.com/9e788289-6545-4e5e-9d00-f284b2337fcd">WSPSendTo</a>
 

 

