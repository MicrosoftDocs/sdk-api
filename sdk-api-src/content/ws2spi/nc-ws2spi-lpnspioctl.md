---
UID: NC:ws2spi.LPNSPIOCTL
title: LPNSPIOCTL
author: windows-sdk-content
description: Sends an IOCTL to a namespace service provider.
old-location: winsock\nspioctl.htm
old-project: WinSock
ms.assetid: 061969f5-dbb5-47d7-820d-5af6fe6a0c62
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: LPNSPIOCTL, NSPIoctl, NSPIoctl function [Winsock], SIO_NSP_NOTIFY_CHANGE, winsock.nspioctl, ws2spi/NSPIoctl
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: ws2spi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SOCKADDR_INET, *PSOCKADDR_INET
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ws2spi.h
api_name:
 - NSPIoctl
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# LPNSPIOCTL callback function


## -description


The <b>NSPIoctl</b> function sends  an IOCTL to a namespace service provider.


## -parameters




### -param hLookup [in]

The lookup handle returned from a previous call to the 
<a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPLookupServiceBegin</a> function. 


### -param dwControlCode [in]

The control code of the operation to perform.


The values that may be used for the <i>dwControlCode</i> parameter are determined by the namespace provider. 

The following value is supported by several Microsoft namespace providers including the Network Location Awareness (NS_NLA) namespace provider. This IOCTL is defined in the Winsock2.h header file.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SIO_NSP_NOTIFY_CHANGE"></a><a id="sio_nsp_notify_change"></a><dl>
<dt><b>SIO_NSP_NOTIFY_CHANGE</b></dt>
</dl>
</td>
<td width="60%">
This operation checks if the results returned with previous calls using the <i>hLookup</i> parameter are still valid.  These previous calls include the initial call to the <a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPLookupServiceBegin</a> function to retrieve the <i>hLookup</i> parameter.  These previous calls may also include calls to the <a href="https://msdn.microsoft.com/321732e4-5d48-48f4-8795-ffac208852dc">NSPLookupServiceNext</a> function using the <i>hLookup</i> parameter. 

</td>
</tr>
</table>
 


### -param lpvInBuffer [in]

A pointer to the input buffer.


### -param cbInBuffer [in, out]

The size, in bytes, of the input buffer.


### -param lpvOutBuffer [out]

A pointer to the output buffer.


### -param cbOutBuffer [in]

The size, in bytes, of the output buffer.


### -param lpcbBytesReturned [out]

A pointer to the number of bytes returned.


### -param lpCompletion [in]

A pointer to a <a href="https://msdn.microsoft.com/5af4b4d1-6dcb-4fc8-a730-53a8cb92fee4">WSACOMPLETION</a> structure, used for asynchronous processing. Set <i>lpCompletion</i> to <b>NULL</b> to force blocking (synchronous) execution.


### -param lpThreadId [in]

A pointer to a 
<a href="https://msdn.microsoft.com/eeea1139-1d14-4f53-bd64-833539b53bed">WSATHREADID</a> structure to be used by the provider in a subsequent call to 
<a href="https://msdn.microsoft.com/4326547e-85e2-409c-9f36-aa013853dfd9">WPUQueueApc</a>. The provider should store the referenced 
<b>WSATHREADID</b> structure (not the pointer) until after the 
<b>WPUQueueApc</b> function returns.


## -returns



If no error occurs and the operation has completed immediately, 
the <b>NSPIoctl</b> function should return <b>NO_ERROR</b> (zero). Note that in this case the completion routine, if specified, will have already been queued. 

The <b>NSPIoctl</b> function should return <b>SOCKET_ERROR</b> (â€“1) if the routine fails and it must set the appropriate error code using 
<a href="https://msdn.microsoft.com/596155ee-3dcc-4ae3-97ab-0653e019cbee">WSASetLastError</a>. 

The error code WSA_IO_PENDING indicates that an overlapped operation has been successfully initiated and that completion will be indicated at a later time. Any other error code indicates that no overlapped operation was initiated and no completion indication will occur.
					

<table>
<tr>
<th>Error code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSA_INVALID_HANDLE</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>hLookup</i> parameter was not a valid query handle returned by 
<a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPLookupServiceBegin</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSA_IO_PENDING</a></b></dt>
</dl>
</td>
<td width="60%">
An overlapped operation was successfully initiated and completion will be indicated at a later time.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>lpvInBuffer</i>, <i>cbInBuffer</i>, <i>lpvOutBuffer</i>, <i>cbOutBuffer</i>, or <i>lpCompletion</i> argument is not totally contained in a valid part of the user address space. Alternatively, the <i>cbInBuffer</i> or <i>cbOutBuffer</i> argument is too small, and the argument is modified to reflect the required allocation size.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
A supplied parameter is not acceptable, or the operation inappropriately returns results from multiple namespaces when it does not make sense for the specified operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAENETDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
The network subsystem has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEOPNOTSUPP</a></b></dt>
</dl>
</td>
<td width="60%">
The operation is not supported. This error is returned if the namespace provider does not implement this function. This error can also be returned if the specified <i>dwControlCode</i> is an unrecognized command.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEWOULDBLOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The resource is temporarily unavailable. The socket is not using overlapped I/O (asynchronous processing), yet the <i>lpCompletion</i> parameter is non-<b>NULL</b>. 

This error is used as a special notification for the SIO_NSP_NOTIFY_CHANGE IOCTL when the <i>lpCompletion</i> parameter is <b>NULL</b> (a poll) to indicate that a query set remains valid.

</td>
</tr>
</table>
 




## -remarks



The 
<b>NSPIoctl</b> function is used to send an I/O control code to a namespace provider in order to set or retrieve operating parameters associated with a query handle. The <i>hLookup</i> parameter is a handle to the namespace provider query previously returned by 
the <a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPLookupServiceBegin</a> function (not  a socket handle).

Any IOCTL sent to a namespace provider may block indefinitely, depending upon the implementation of the namespace. If an application cannot tolerate blocking in a 
<b>NSPIoctl</b> function call, overlapped I/O should be used and the <i>lpCompletion</i> parameter should point to a <a href="https://msdn.microsoft.com/5af4b4d1-6dcb-4fc8-a730-53a8cb92fee4">WSACOMPLETION</a> structure. To make a 
<b>NSPIoctl</b> function call nonblocking and return immediately, set the <b>Type</b> member of the <b>WSACOMPLETION</b> structure to <b>NSP_NOTIFY_IMMEDIATELY</b>.

 If <i>lpCompletion</i> is <b>NULL</b>, the 
<b>NSPIoctl</b> function executes as a blocking call. The namespace provider should return immediately and should not block. But each namespace provider is responsible for enforcing this behavior. 

The following IOCTL code is supported by several Microsoft namespace providers:




<dl>
<dt><a id="SIO_NSP_NOTIFY_CHANGE"></a><a id="sio_nsp_notify_change"></a><b>SIO_NSP_NOTIFY_CHANGE</b></dt>
<dd>
This operation checks if the results returned with previous calls using the <i>hLookup</i> parameter are still valid.  These previous calls include the initial call to the <a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPLookupServiceBegin</a> function to retrieve the <i>hLookup</i> parameter.  These previous calls may also include calls to the <a href="https://msdn.microsoft.com/321732e4-5d48-48f4-8795-ffac208852dc">NSPLookupServiceNext</a> function using the <i>hLookup</i> parameter. 

The Microsoft namespace providers that support this IOCTL include the following:


<ul>
<li>NS_NLA - The Network Location Awareness (NLA) namespace provider.</li>
<li>NS_PNRPNAME - The Peer Name Resolution Protocol (PNRP) namespace provider.</li>
<li>NS_PNRPCLOUD - The Peer Name Resolution Protocol (PNRP) cloud namespace provider.</li>
</ul>


Other non-Microsoft namespace providers may be installed that also support this IOCTL.

When the <i>lpCompletion</i> parameter is <b>NULL</b>, this IOCTL implements a  special behavior. If the <i>lpCompletion</i> parameter is <b>NULL</b> for this IOCTL, this operation is a poll and returns immediately. If the query set remains valid, 
<a href="windows_sockets_error_codes_2.htm">WSAEWOULDBLOCK</a> is returned as notification that the query set remains valid. If the query set has changed and is invalid, <b>NO_ERROR</b> is returned indicating success in polling for invalidation of the query set. 

If the <i>lpCompletion</i> parameter is not <b>NULL</b> and points to an <a href="https://msdn.microsoft.com/5af4b4d1-6dcb-4fc8-a730-53a8cb92fee4">WSACOMPLETION</a> structure, then the  <b>NSPIoctl</b> function returns <a href="windows_sockets_error_codes_2.htm">WSA_IO_PENDING</a> if the  overlapped operation was successfully initiated and completion will be indicated at a later time. The method specified in the <b>WSACOMPLETION</b> structure is used to notify the application if the query set is still valid. 

Not all name resolution protocols are able to support this feature, and therefore, this function call may fail with 
<a href="windows_sockets_error_codes_2.htm">WSAEOPNOTSUPP</a>. A query containing data from multiple providers cannot call this IOCTL, and will return 
<a href="windows_sockets_error_codes_2.htm">WSAEINVAL</a>.

The <i>lpvInBuffer</i>, <i>cbInBuffer</i>, <i>lpvOutBuffer</i>, and <i>cbOutBuffer</i> parameters are currently ignored by Microsoft namespace providers.

For single-threaded applications, a typical method to use the <b>NSPIoctl</b> function is as follows. Call the <b>NSPIoctl</b> function with the <i>dwControlCode</i> parameter set to <b>SIO_NSP_NOTIFY_CHANGE</b> with no completion routine (the <i>lpCompletion</i> parameter set to <b>NULL</b>) after every <a href="https://msdn.microsoft.com/321732e4-5d48-48f4-8795-ffac208852dc">NSPLookupServiceNext</a> function  call to make sure the query data is still valid. If the data becomes invalid, call the <a href="https://msdn.microsoft.com/ec72c89a-a74b-449c-996a-02057dff9137">NSPLookupServiceEnd</a>function to close the query handle. Call the <a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPLookupServiceBegin</a> function to retrieve a new query handle and begin the query again.

For multithreaded applications, a typical method to use the <b>NSPIoctl</b> function is as follows. Call the <b>NSPIoctl</b> function with the <i>dwControlCode</i> parameter set to <b>SIO_NSP_NOTIFY_CHANGE</b> with a completion routine after the initial call to the <a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPLookupServiceBegin</a> function. The application would use the mechanism for notification specified in the completion routine to be notified when data is no longer valid. One common mechanism is to use an event specified in the completion routine. If the data becomes invalid, call the <a href="https://msdn.microsoft.com/ec72c89a-a74b-449c-996a-02057dff9137">NSPLookupServiceEnd</a>function to close the query handle. Call the <b>NSPLookupServiceBegin</b> and the <b>NSPIoctl</b> functions to retrieve a new query handle and begin the query again.

Some protocols may simply cache the information locally and invalidate it after some time, in which case notification may be issued to indicate the local cache has been invalidated.

For name resolution protocols where changes are infrequent, it is possible for a namespace provider to indicate a global change event that may not be applicable to the query on which change notification was requested and issued.

</dd>
</dl>


Immediate poll operations are usually much less resource intensive since they do not require a notification object. In most cases, this is implemented as a simple Boolean variable check. Asynchronous notification, however, may necessitate the creation of dedicated worker threads and/or inter-process communication channels, depending on the implementation of the namespace provider service, and will incur processing overhead related to the notification object involved with signaling the change event.

To cancel an asynchronous notification request, end the original query with a 
<a href="https://msdn.microsoft.com/ec72c89a-a74b-449c-996a-02057dff9137">NSPLookupServiceEnd</a> function call on the affected query handle. Canceling the asynchronous notification for LUP_NOTIFY_HWND will not post any message, however, an overlapped operation will be completed and notification will be delivered with the error 
<a href="windows_sockets_error_codes_2.htm">WSA_OPERATION_ABORTED</a>.

<div class="alert"><b>Note</b>   All I/O initiated by a given thread is canceled when that thread exits. For overlapped sockets, pending asynchronous operations can fail if the thread is closed before the  operations complete. See <a href="https://msdn.microsoft.com/e7f6d054-c535-4521-a3b4-800a9174732f">ExitThread</a> for more information.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPLookupServiceBegin</a>



<a href="https://msdn.microsoft.com/ec72c89a-a74b-449c-996a-02057dff9137">NSPLookupServiceEnd</a>



<a href="https://msdn.microsoft.com/321732e4-5d48-48f4-8795-ffac208852dc">NSPLookupServiceNext</a>



<a href="https://msdn.microsoft.com/ed9e4ff3-736a-4037-bf85-5572f0cd279d">NSPStartup</a>



<a href="https://msdn.microsoft.com/8f7736d5-ea77-472a-a94f-e422398fae3f">NSP_ROUTINE</a>



<a href="https://msdn.microsoft.com/4326547e-85e2-409c-9f36-aa013853dfd9">WPUQueueApc</a>



<a href="https://msdn.microsoft.com/5af4b4d1-6dcb-4fc8-a730-53a8cb92fee4">WSACOMPLETION</a>



<a href="https://msdn.microsoft.com/eeea1139-1d14-4f53-bd64-833539b53bed">WSATHREADID</a>
 

 

