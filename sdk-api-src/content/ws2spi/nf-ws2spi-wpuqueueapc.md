---
UID: NF:ws2spi.WPUQueueApc
title: WPUQueueApc function (ws2spi.h)
author: windows-sdk-content
description: The WPUQueueApc function queues a user mode&#8211;asynchronous procedure call (APC) to the specified thread in order to facilitate invocation of overlapped I/O completion routines.
old-location: winsock\wpuqueueapc_2.htm
tech.root: WinSock
ms.assetid: 4326547e-85e2-409c-9f36-aa013853dfd9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WPUQueueApc, WPUQueueApc function [Winsock], _win32_wpuqueueapc_2, winsock.wpuqueueapc_2, ws2spi/WPUQueueApc
ms.topic: function
f1_keywords:
- ws2spi/WPUQueueApc
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WPUQueueApc function


## -description


The 
<b>WPUQueueApc</b> function queues a user mode–asynchronous procedure call (APC) to the specified thread in order to facilitate invocation of overlapped I/O completion routines.


## -parameters




### -param lpThreadId [in]

Pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid">WSATHREADID</a> structure that identifies the thread context. A pointer to this structure is supplied to the service provider by the Ws2_32.dll as an input parameter to an overlapped operation. The provider should store the 
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
<dt><b><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
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




<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid">WSATHREADID</a>



<a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566296(v=vs.85)">LPWSPIoctl</a>



<a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566309(v=vs.85)">WSPRecv</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)">LPWSPRecvFrom</a>



<a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566316(v=vs.85)">WSPSend</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)">WSPSendTo</a>
 

 

