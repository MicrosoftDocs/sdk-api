---
UID: NF:winsock2.WSANSPIoctl
title: WSANSPIoctl function (winsock2.h)
description: Enables developers to make I/O control calls to a registered namespace.
helpviewer_keywords: ["SIO_NSP_NOTIFY_CHANGE","WSANSPIoctl","WSANSPIoctl function [Winsock]","_win32_wsanspioctl_2","winsock.wsanspioctl_2","winsock2/WSANSPIoctl"]
old-location: winsock\wsanspioctl_2.htm
tech.root: WinSock
ms.assetid: 6ecaedf0-0038-46d3-9916-c9cb069c5e92
ms.date: 12/05/2018
ms.keywords: SIO_NSP_NOTIFY_CHANGE, WSANSPIoctl, WSANSPIoctl function [Winsock], _win32_wsanspioctl_2, winsock.wsanspioctl_2, winsock2/WSANSPIoctl
req.header: winsock2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WSANSPIoctl
 - winsock2/WSANSPIoctl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winsock2.h
api_name:
 - WSANSPIoctl
---

# WSANSPIoctl function


## -description

The Windows Sockets 
<b>WSANSPIoctl</b> function enables developers to make I/O control calls to a registered namespace.

## -parameters

### -param hLookup [in]

The lookup handle returned from a previous call to the 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina">WSALookupServiceBegin</a> function.

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
This operation checks if the results returned with previous calls using the <i>hLookup</i> parameter are still valid.  These previous calls include the initial call to the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina">WSALookupServiceBegin</a> function to retrieve the <i>hLookup</i> parameter.  These previous calls may also include calls to the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta">WSALookupServiceNext</a> function using the <i>hLookup</i> parameter. 

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

A pointer to a <a href="/windows/desktop/api/winsock2/ns-winsock2-wsacompletion">WSACOMPLETION</a> structure, used for asynchronous processing. Set <i>lpCompletion</i> to <b>NULL</b> to force blocking (synchronous) execution.

## -returns

Success returns NO_ERROR. Failure returns SOCKET_ERROR, and a specific error code can be retrieved by calling the 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a> function. The following table describes the error codes.

<table>
<tr>
<th>Error code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_INVALID_HANDLE</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>hLookup</i> parameter was not a valid query handle returned by 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina">WSALookupServiceBegin</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_IO_PENDING</a></b></dt>
</dl>
</td>
<td width="60%">
An overlapped operation was successfully initiated and completion will be indicated at a later time.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>lpvInBuffer</i>, <i>cbInBuffer</i>, <i>lpvOutBuffer</i>, <i>cbOutBuffer</i>, or <i>lpCompletion</i> argument is not totally contained in a valid part of the user address space. Alternatively, the <i>cbInBuffer</i> or <i>cbOutBuffer</i> argument is too small, and the argument is modified to reflect the required allocation size.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
A supplied parameter is not acceptable, or the operation inappropriately returns results from multiple namespaces when it does not make sense for the specified operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENETDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
The network subsystem has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEOPNOTSUPP</a></b></dt>
</dl>
</td>
<td width="60%">
The operation is not supported. This error is returned if the namespace provider does not implement this function. This error can also be returned if the specified <i>dwControlCode</i> is an unrecognized command.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEWOULDBLOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The socket is not using overlapped I/O (asynchronous processing), yet the <i>lpCompletion</i> parameter is non-<b>NULL</b>.

This error is used as a special notification for the SIO_NSP_NOTIFY_CHANGE IOCTL when the <i>lpCompletion</i> parameter is <b>NULL</b> (a poll) to indicate that a query set remains valid.

</td>
</tr>
</table>

## -remarks

The 
<b>WSANSPIoctl</b> function is used to set or retrieve operating parameters associated with a query handle to a namespace provider. The <i>hLookup</i> parameter is a handle to the namespace provider query previously returned by 
the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina">WSALookupServiceBegin</a> function (not  a socket handle).

Any IOCTL sent to a namespace provider may block indefinitely, depending upon the implementation of the namespace. If an application cannot tolerate blocking in a 
<b>WSANSPIoctl</b> function call, overlapped I/O should be used and the <i>lpCompletion</i> parameter should point to a <a href="/windows/desktop/api/winsock2/ns-winsock2-wsacompletion">WSACOMPLETION</a> structure. To make a 
<b>WSANSPIoctl</b> function call nonblocking and return immediately, set the <b>Type</b> member of the <b>WSACOMPLETION</b> structure to <b>NSP_NOTIFY_IMMEDIATELY</b>.

 If <i>lpCompletion</i> is <b>NULL</b>, the 
<b>WSANSPIoctl</b> function executes as a blocking call. The namespace provider should return immediately and should not block. But each namespace is responsible for enforcing this behavior. 

The following IOCTL code is supported by several Microsoft name space provider:

<dl>
<dt><a id="SIO_NSP_NOTIFY_CHANGE"></a><a id="sio_nsp_notify_change"></a><b>SIO_NSP_NOTIFY_CHANGE</b></dt>
<dd>
This operation checks if the results returned with previous calls using the <i>hLookup</i> parameter are still valid.  These previous calls include the initial call to the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina">WSALookupServiceBegin</a> function to retrieve the <i>hLookup</i> parameter.  These previous calls may also include calls to the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta">WSALookupServiceNext</a> function using the <i>hLookup</i> parameter. 

The Microsoft namespace providers that support this IOCTL include the following<ul>
<li>NS_NLA - The Network Location Awareness (NLA) namespace provider.</li>
<li>NS_PNRPNAME - The Peer Name Resolution Protocol (PNRP) namespace provider.</li>
<li>NS_PNRPCLOUD - The Peer Name Resolution Protocol (PNRP) cloud namespace provider.</li>
</ul>


Other non-Microsoft namespace providers may be installed that also support this IOCTL.

When the <i>lpCompletion</i> parameter is <b>NULL</b>, this IOCTL implements a  special behavior. If the <i>lpCompletion</i> parameter is <b>NULL</b> for this IOCTL, this operation is a poll and returns immediately. If the query set remains valid, 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEWOULDBLOCK</a> is returned as notification that the query set remains valid. If the query set has changed and is invalid, <b>NO_ERROR</b> is returned indicating success in polling for invalidation of the query set. 

If the <i>lpCompletion</i> parameter is not <b>NULL</b> and points to an <a href="/windows/desktop/api/winsock2/ns-winsock2-wsacompletion">WSACOMPLETION</a> structure, then the  <b>WSANSPIoctl</b> function returns <a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_IO_PENDING</a> if the  overlapped operation was successfully initiated and completion will be indicated at a later time. The method specified in the <b>WSACOMPLETION</b> structure is used to notify the application if the query set is still valid. 

Not all name resolution protocols are able to support this feature, and therefore, this function call may fail with 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEOPNOTSUPP</a>. A query containing data from multiple providers cannot call this IOCTL, and will return 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a>.

The <i>lpvInBuffer</i>, <i>cbInBuffer</i>, <i>lpvOutBuffer</i>, and <i>cbOutBuffer</i> parameters are currently ignored by Microsoft namespace providers.

For single-threaded applications, a typical method to use the <b>WSANSPIoctl</b> function is as follows. Call the <b>WSANSPIoctl</b> function with the <i>dwControlCode</i> parameter set to <b>SIO_NSP_NOTIFY_CHANGE</b> with no completion routine (the <i>lpCompletion</i> parameter set to <b>NULL</b>) after every <a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta">WSALookupServiceNext</a> function  call to make sure the query data is still valid. If the data becomes invalid, call the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend">WSALookupServiceEnd</a> function to close the query handle. Call the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina">WSALookupServiceBegin</a> function to retrieve a new query handle and begin the query again.

For multi-threaded applications, a typical method to use the <b>WSANSPIoctl</b> function is as follows. Call the <b>WSANSPIoctl</b> function with the <i>dwControlCode</i> parameter set to <b>SIO_NSP_NOTIFY_CHANGE</b> with a completion routine after the initial call to the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina">WSALookupServiceBegin</a> function. The application would use the mechanism for notification specified in the completion routine to be notified when data is no longer valid. One common mechanism is to use an event specified in the completion routine. If the data becomes invalid, call the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend">WSALookupServiceEnd</a> function to close the query handle. Call the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina">WSALookupServiceBegin</a> and the <b>WSANSPIoctl</b> functions to retrieve a new query handle and begin the query again.

Some protocols may simply cache the information locally and invalidate it after some time, in which case notification may be issued to indicate the local cache has been invalidated.

For name resolution protocols where changes are infrequent, it is possible for a namespace provider to indicate a global change event that may not be applicable to the query on which change notification was requested and issued.

</dd>
</dl>


Immediate poll operations are usually much less expensive since they do not require a notification object. In most cases, this is implemented as a simple Boolean variable check. Asynchronous notification, however, may necessitate the creation of dedicated worker threads and/or inter-process communication channels, depending on the implementation of the namespace provider service, and will incur processing overhead related to the notification object involved with signaling the change event.

To cancel an asynchronous notification request, end the original query with a 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend">WSALookupServiceEnd</a> function call on the affected query handle. Canceling the asynchronous notification for LUP_NOTIFY_HWND will not post any message, however, an overlapped operation will be completed and notification will be delivered with the error 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_OPERATION_ABORTED</a>.

<div class="alert"><b>Note</b>   All I/O initiated by a given thread is canceled when that thread exits. For overlapped sockets, pending asynchronous operations can fail if the thread is closed before the  operations complete. See <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread">ExitThread</a> for more information.</div>
<div> </div>
<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread">ExitThread</a>



<a href="/windows/desktop/api/winsock2/ns-winsock2-wsacompletion">WSACOMPLETION</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina">WSALookupServiceBegin</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend">WSALookupServiceEnd</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta">WSALookupServiceNext</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>