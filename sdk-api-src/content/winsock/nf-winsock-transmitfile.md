---
UID: NF:winsock.TransmitFile
title: TransmitFile function (winsock.h)
description: The TransmitFile function (winsock.h) transmits file data over a connected socket handle.
old-location: winsock\transmitfile_2.htm
tech.root: WinSock
ms.assetid: 45db763e-735d-48ac-a0e4-6e63b5dda7a5
ms.date: 08/16/2022
ms.keywords: LPFN_TRANSMITFILE, LPFN_TRANSMITFILE function [Winsock], TF_DISCONNECT, TF_REUSE_SOCKET, TF_USE_DEFAULT_WORKER, TF_USE_KERNEL_APC, TF_USE_SYSTEM_THREAD, TF_WRITE_BEHIND, TransmitFile, TransmitFile function [Winsock], _win32_transmitfile_2, winsock.transmitfile_2, winsock/LPFN_TRANSMITFILE, winsock/TransmitFile
req.header: winsock.h
req.include-header: Mswsock.h
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
req.lib: Mswsock.lib
req.dll: Mswsock.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TransmitFile
 - winsock/TransmitFile
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mswsock.dll
api_name:
 - TransmitFile
---

# TransmitFile function


## -description

The 
<b>TransmitFile</b> function transmits file data over a connected socket handle. This function uses the operating system's cache manager to retrieve the file data, and provides high-performance file data transfer over sockets.<div class="alert"><b>Note</b>  This function is a Microsoft-specific extension to the Windows Sockets specification.</div>
<div> </div>

## -parameters

### -param hSocket

A handle to a connected socket. The 
<b>TransmitFile</b> function will transmit the file data over this socket. The socket specified by the <i>hSocket</i> parameter must be a connection-oriented socket of type <b>SOCK_STREAM</b>, <b>SOCK_SEQPACKET</b>, or <b>SOCK_RDM</b>.

### -param hFile

A handle to the open file that the 
<b>TransmitFile</b> function transmits. Since the operating system reads the file data sequentially, you can improve caching performance by opening the handle with FILE_FLAG_SEQUENTIAL_SCAN. 

The <i>hFile</i> parameter is optional. If the <i>hFile</i> parameter is <b>NULL</b>, only data in the header and/or the tail buffer is transmitted. Any additional action, such as socket disconnect or reuse, is performed as specified by the <i>dwFlags</i> parameter.

### -param nNumberOfBytesToWrite

The number of bytes in the file to transmit. The 
<b>TransmitFile</b> function completes when it has sent the specified number of bytes, or when an error occurs, whichever occurs first. 




Set this parameter to zero in order to transmit the entire file.

### -param nNumberOfBytesPerSend

The size, in bytes, of each block of data sent in each send operation. This parameter is used by Windows' sockets layer to determine the block size for send operations. To select the default send size, set this parameter to zero.

The <i>nNumberOfBytesPerSend</i> parameter is useful for protocols that have limitations on the size of individual send requests.

### -param lpOverlapped

A pointer to an 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure. If the socket handle has been opened as overlapped, specify this parameter in order to achieve an overlapped (asynchronous) I/O operation. By default, socket handles are opened as overlapped. 




You can use the <i>lpOverlapped</i> parameter to specify a 64-bit offset within the file at which to start the file data transfer by setting the <b>Offset</b> and <b>OffsetHigh</b> member of the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure. If <i>lpOverlapped</i> is a <b>NULL</b> pointer, the transmission of data always starts at the current byte offset in the file.

When the <i>lpOverlapped</i> is not <b>NULL</b>, the overlapped I/O might not finish before 
<b>TransmitFile</b> returns. In that case, the 
<b>TransmitFile</b> function returns <b>FALSE</b>, and <a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a> returns ERROR_IO_PENDING or <a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_IO_PENDING</a>. This enables the caller to continue processing while the file transmission operation completes. Windows will set the event specified by the <b>hEvent</b> member of the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure, or the socket specified by <i>hSocket</i>, to the signaled state upon completion of the data transmission request.

### -param lpTransmitBuffers

A pointer to a 
<a href="/windows/desktop/api/mswsock/ns-mswsock-transmit_file_buffers">TRANSMIT_FILE_BUFFERS</a> data structure that contains pointers to data to send before and after the file data is sent. This parameter should be set to a <b>NULL</b> pointer if you want to transmit only the file data.

### -param dwReserved

A set of flags used to modify the behavior of the <b>TransmitFile</b> function call. The <i>dwFlags</i> parameter can contain a combination of the following options defined in the <i>Mswsock.h</i> header file: 



<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TF_DISCONNECT"></a><a id="tf_disconnect"></a><dl>
<dt><b>TF_DISCONNECT</b></dt>
</dl>
</td>
<td width="60%">
Start a transport-level disconnect after all the file data has been queued for transmission.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_REUSE_SOCKET"></a><a id="tf_reuse_socket"></a><dl>
<dt><b>TF_REUSE_SOCKET</b></dt>
</dl>
</td>
<td width="60%">
Prepare the socket handle to be reused. This flag is valid only if <b>TF_DISCONNECT</b> is also specified.

When the <b>TransmitFile</b> request completes, the socket handle can be passed to the 
function call previously used to establish the connection, such as <a href="/windows/desktop/api/mswsock/nf-mswsock-acceptex">AcceptEx</a>  or <a href="/windows/desktop/api/mswsock/nc-mswsock-lpfn_connectex">ConnectEx</a>. Such reuse is mutually exclusive; for example, if the <b>AcceptEx</b> function was called for the socket, reuse is allowed only for subsequent calls to the <b>AcceptEx</b>  function, and not allowed for a subsequent call to <b>ConnectEx</b>. 

<div class="alert"><b>Note</b>  The socket level file transmit is subject to the behavior of the underlying transport. For example, a TCP socket may be subject to the TCP TIME_WAIT state, causing  the <b>TransmitFile</b> call to be delayed.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="TF_USE_DEFAULT_WORKER"></a><a id="tf_use_default_worker"></a><dl>
<dt><b>TF_USE_DEFAULT_WORKER</b></dt>
</dl>
</td>
<td width="60%">
Directs the Windows Sockets service provider to use the system's default thread to process long <b>TransmitFile</b> requests. The system default thread can be adjusted using the following registry parameter as a <b>REG_DWORD</b>:


<b>HKEY_LOCAL_MACHINE</b>&#92;<b>CurrentControlSet</b>&#92;<b>Services</b>&#92;<b>AFD</b>&#92;<b>Parameters</b>&#92;<b>TransmitWorker</b>



</td>
</tr>
<tr>
<td width="40%"><a id="TF_USE_SYSTEM_THREAD"></a><a id="tf_use_system_thread"></a><dl>
<dt><b>TF_USE_SYSTEM_THREAD</b></dt>
</dl>
</td>
<td width="60%">
Directs the Windows Sockets service provider to use system threads to process long 
<b>TransmitFile</b> requests.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_USE_KERNEL_APC"></a><a id="tf_use_kernel_apc"></a><dl>
<dt><b>TF_USE_KERNEL_APC</b></dt>
</dl>
</td>
<td width="60%">
Directs the driver to use kernel asynchronous procedure calls (APCs) instead of worker threads to process long 
<b>TransmitFile</b> requests. Long <b>TransmitFile</b> requests are defined as requests that require more than a single read from the file or a cache; the request therefore depends on the size of the file and the specified length of the send packet.

Use of TF_USE_KERNEL_APC can deliver significant performance benefits. It is possible (though unlikely), however, that the thread in which context 
<b>TransmitFile</b> is initiated is being used for heavy computations; this situation may prevent APCs from launching. Note that the Winsock kernel mode driver uses normal kernel APCs, which launch whenever a thread is in a wait state, which differs from user-mode APCs, which launch whenever a thread is in an alertable wait state initiated in user mode).

</td>
</tr>
<tr>
<td width="40%"><a id="TF_WRITE_BEHIND"></a><a id="tf_write_behind"></a><dl>
<dt><b>TF_WRITE_BEHIND</b></dt>
</dl>
</td>
<td width="60%">
Complete the 
<b>TransmitFile</b> request immediately, without pending. If this flag is specified and 
<b>TransmitFile</b> succeeds, then the data has been accepted by the system but not necessarily acknowledged by the remote end. Do not use this setting with the TF_DISCONNECT and TF_REUSE_SOCKET flags.

<div class="alert"><b>Note</b>  If the file being sent is not in the file system cache, the request  pends.</div>
<div> </div>
</td>
</tr>
</table>

## -returns

If the 
<b>TransmitFile</b> function succeeds, the return value is <b>TRUE</b>. Otherwise, the return value is <b>FALSE</b>. To get extended error information, call 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>. An error code 
of <a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_IO_PENDING</a> or ERROR_IO_PENDING indicates that the overlapped operation has been successfully initiated and that completion will be indicated at a later time. Any other error code indicates that the overlapped operation was not successfully initiated and no completion indication will occur. Applications should handle either ERROR_IO_PENDING or WSA_IO_PENDING in this case.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAECONNABORTED</a></b></dt>
</dl>
</td>
<td width="60%">
An established connection was aborted by the software in your host machine. This error is returned if the virtual circuit was terminated due to a time-out or other failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAECONNRESET</a></b></dt>
</dl>
</td>
<td width="60%">
An existing connection was forcibly closed by the remote host. This error is returned for a stream socket when the virtual circuit was reset by the remote side. The application should close the socket as it is no longer usable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The system detected an invalid pointer address in attempting to use a pointer argument in a call. This error is returned if the <i>lpTransmitBuffers</i> or <i>lpOverlapped</i> parameter is not totally contained in a valid part of the user address space.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
An invalid argument was supplied. This error is returned if the <i>hSocket</i> parameter specified a socket of type <b>SOCK_DGRAM</b> or <b>SOCK_RAW</b>. This error is returned if the <i>dwFlags</i> parameter has the  <b>TF_REUSE_SOCKET</b> flag set, but the <b>TF_DISCONNECT</b> flag was not set. This error is also returned if the offset specified in the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure pointed to by the <i>lpOverlapped</i> is not within the file. This error is also returned if the <i>nNumberOfBytesToWrite</i> parameter is set to a value greater than  2,147,483,646, the maximum value for a 32-bit integer minus 1.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENETDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
A socket operation encountered a dead network.This error is returned if the network subsystem has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENETRESET</a></b></dt>
</dl>
</td>
<td width="60%">
The connection has been broken due to keep-alive activity detecting a failure while the operation was in progress. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOBUFS</a></b></dt>
</dl>
</td>
<td width="60%">
An operation on a socket could not be performed because the system lacked sufficient buffer space or because a queue was full. This error is also returned if the Windows Sockets provider reports a buffer deadlock.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOTCONN</a></b></dt>
</dl>
</td>
<td width="60%">
A request to send or receive data was disallowed because the socket is not connected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOTSOCK</a></b></dt>
</dl>
</td>
<td width="60%">
An operation was attempted on something that is not a socket. This error is returned if the <i>hSocket</i> parameter is not a socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAESHUTDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
A request to send or receive data was disallowed because the socket had already been shut down in that direction with a previous shutdown call. This error is returned if the socket has been shut down for sending. It is not possible to 
call <a href="/windows/desktop/api/mswsock/nf-mswsock-transmitfile">TransmitFile</a> on a socket after 
the <a href="/windows/desktop/api/winsock/nf-winsock-shutdown">shutdown</a> function has been called on the socket with the <i>how</i> parameter set to <b>SD_SEND</b> or <b>SD_BOTH</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANOTINITIALISED</a></b></dt>
</dl>
</td>
<td width="60%">
Either the application has not called the <a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a> function, or <b>WSAStartup</b> failed. A successful 
<b>WSAStartup</b> call must occur before using the <a href="/windows/desktop/api/mswsock/nf-mswsock-transmitfile">TransmitFile</a> function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_IO_PENDING</a></b></dt>
</dl>
</td>
<td width="60%">
An overlapped I/O operation is in progress. This value is returned if an overlapped I/O operation was successfully initiated and indicates that completion will be indicated at a later time.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_OPERATION_ABORTED</a></b></dt>
</dl>
</td>
<td width="60%">
The I/O operation has been aborted because of either a thread exit or an application request. This error is returned if the overlapped operation has been canceled due to the closure of the socket, the execution of the "SIO_FLUSH" command in 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a>, or the thread that initiated the overlapped request exited before the operation completed.

<div class="alert"><b>Note</b>  All I/O initiated by a given thread is canceled when that thread exits. For overlapped sockets, pending asynchronous operations can fail if the thread is closed before the  asynchronous operations complete. For more information, see <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread">ExitThread</a>.</div>
<div> </div>
</td>
</tr>
</table>

## -remarks

The <b>TransmitFile</b> function uses the operating system's cache manager to retrieve the file data, and provide high-performance file data transfer over sockets.

The <b>TransmitFile</b> function only supports connection-oriented sockets of type <b>SOCK_STREAM</b>, <b>SOCK_SEQPACKET</b>, and <b>SOCK_RDM</b>. Sockets of type <b>SOCK_DGRAM</b> and <b>SOCK_RAW</b> are not supported. The <a href="/windows/desktop/api/mswsock/nc-mswsock-lpfn_transmitpackets">TransmitPackets</a> function can be used with sockets of type <b>SOCK_DGRAM</b>. 

The maximum number of bytes that can be transmitted using a single call to the <b>TransmitFile</b> function is 2,147,483,646, the maximum value for a 32-bit integer minus 1. The maximum number of bytes to send in a single call includes any  data sent before or after the file data pointed to by the <i>lpTransmitBuffers</i> parameter plus the value specified in the <i>nNumberOfBytesToWrite</i> parameter for the length of file data to send. If an application needs to transmit a file larger than 2,147,483,646 bytes, then multiple calls to the <b>TransmitFile</b> function can be used with each call transferring no more than 2,147,483,646 bytes. Setting the <i>nNumberOfBytesToWrite</i> parameter to zero for a file larger than 2,147,483,646 bytes will also fail since in this case the <b>TransmitFile</b> function will use the size of the file as the value for the number of bytes to transmit.


<div class="alert"><b>Note</b>  The function pointer for the 
<b>TransmitFile</b> function must be obtained at run time by making a call to the 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a> function with the <b>SIO_GET_EXTENSION_FUNCTION_POINTER</b> opcode specified. The input buffer passed to the <b>WSAIoctl</b> function must contain <b>WSAID_TRANSMITFILE</b>, a globally unique identifier (GUID) whose value identifies the <b>TransmitFile</b> extension function. On success, the output returned by the <b>WSAIoctl</b> function contains a pointer to the <b>TransmitFile</b> function. The <b>WSAID_TRANSMITFILE</b> GUID is defined in the <i>Mswsock.h</i> header file.</div>
<div> </div>


<div class="alert"><b>Note</b>  <b>TransmitFile</b> is not functional on transports that perform their own buffering. Transports with the TDI_SERVICE_INTERNAL_BUFFERING flag set, such as ADSP, perform their own buffering. Because 
<b>TransmitFile</b> achieves its performance gains by sending data directly from the file cache. Transports that run out of buffer space on a particular connection are not handled by 
<b>TransmitFile</b>, and as a result of running out of buffer space on the connection, 
<b>TransmitFile</b> returns STATUS_DEVICE_NOT_READY.</div>
<div> </div>
The <b>TransmitFile</b> function was primarily added to Winsock for use by high-performance server applications (web and ftp servers, for example). 

Workstation and client versions of Windows optimize the <b>TransmitFile</b> function for minimum memory and resource utilization by limiting the number of concurrent <b>TransmitFile</b> operations allowed on the system to a maximum of two. On Windows Vista,  Windows XP,
  Windows 2000 Professional, and 
  Windows NT Workstation 3.51 and later only two outstanding <b>TransmitFile</b> requests are handled simultaneously; the third request will wait until one of the previous requests is completed. 

Server versions of Windows optimize the 
<b>TransmitFile</b> function for high performance.  On server versions, there are no default limits placed on the number of concurrent <b>TransmitFile</b> operations allowed on the system. Expect better performance results when using 
<b>TransmitFile</b> on server versions of Windows. On server versions of Windows, it is possible to set a limit on the maximum number of concurrent <b>TransmitFile</b> operations by creating a registry entry and setting a value for the following <b>REG_DWORD</b>:


<b>HKEY_LOCAL_MACHINE</b>&#92;<b>CurrentControlSet</b>&#92;<b>Services</b>&#92;<b>AFD</b>&#92;<b>Parameters</b>&#92;<b>MaxActiveTransmitFileCount</b>



If the <b>TransmitFile</b> function is called with TCP socket (protocol of IPPROTO_TCP) with both the <b>TF_DISCONNECT</b> and <b>TF_REUSE_SOCKET</b> flags specified, the call will not complete until the two following conditions are met.<ul>
<li>All pending receive data sent by remote side (received prior to a FIN from the remote side) on the TCP socket has been read.
</li>
<li> The remote side has closed the connection (completed the graceful TCP connection closure).</li>
</ul>


If the <b>TransmitFile</b> function is called with the <i>lpOverlapped</i> parameter set to <b>NULL</b>, the operation is executed as synchronous I/O. The function will not complete until the file has been sent. 

<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

<h3><a id="Notes_for_QoS"></a><a id="notes_for_qos"></a><a id="NOTES_FOR_QOS"></a>Notes for QoS</h3>
The 
<b>TransmitFile</b> function allows the setting of two flags, TF_DISCONNECT or TF_REUSE_SOCKET, that return the socket to a "disconnected, reusable" state after the file has been transmitted. These flags should not be used on a socket where quality of service has been requested, since the service provider may immediately delete any quality of service associated with the socket before the file transfer has completed. The best approach for a QoS-enabled socket is to simply call the 
<a href="/windows/desktop/api/winsock/nf-winsock-closesocket">closesocket</a> function when the file transfer has completed, rather than relying on these flags.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread">ExitThread</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>



<a href="/windows/desktop/api/mswsock/ns-mswsock-transmit_file_buffers">TRANSMIT_FILE_BUFFERS</a>



<a href="/windows/desktop/api/mswsock/nc-mswsock-lpfn_transmitpackets">TransmitPackets</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasend">WSASend</a>



<a href="/windows/desktop/api/winsock/nf-winsock-closesocket">closesocket</a>
