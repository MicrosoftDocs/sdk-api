---
UID: NF:winsock2.WSAIoctl
title: WSAIoctl function (winsock2.h)
description: The WSAIoctl function controls the mode of a socket.
helpviewer_keywords: ["WSAIoctl","WSAIoctl function [Winsock]","_win32_wsaioctl_2","mstcpip/WSAIoctl","winsock.wsaioctl_2","winsock2/WSAIoctl"]
old-location: winsock\wsaioctl_2.htm
tech.root: WinSock
ms.assetid: 038aeca6-d7b7-4f74-ac69-4536c2e5118b
ms.date: 12/14/2023
ms.keywords: WSAIoctl, WSAIoctl function [Winsock], _win32_wsaioctl_2, mstcpip/WSAIoctl, winsock.wsaioctl_2, winsock2/WSAIoctl
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
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WSAIoctl
 - winsock2/WSAIoctl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - WSAIoctl
---

# WSAIoctl function (winsock2.h)

## -description

The <b>WSAIoctl</b> function controls the mode of a socket.

## -parameters

### -param s [in]

A descriptor identifying a socket.

### -param dwIoControlCode [in]

The control code of operation to perform. See [Winsock IOCTLs](/windows/win32/winsock/winsock-ioctls).

### -param lpvInBuffer [in]

A pointer to the input buffer.

### -param cbInBuffer [in]

The size, in bytes, of the input buffer.

### -param lpvOutBuffer [out]

A pointer to the output buffer.

### -param cbOutBuffer [in]

The size, in bytes, of the output buffer.

### -param lpcbBytesReturned [out]

A pointer to actual number of bytes of output.

### -param lpOverlapped [in]

A pointer to a 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped">WSAOVERLAPPED</a> structure (ignored for non-overlapped sockets).

### -param lpCompletionRoutine [in]

Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](./nc-winsock2-lpwsaoverlapped_completion_routine.md)

<div class="alert"><b>Note</b>  A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets). See Remarks.</div>
<div> </div>

## -returns

Upon successful completion, the 
<b>WSAIoctl</b> returns zero. Otherwise, a value of SOCKET_ERROR is returned, and a specific error code can be retrieved by calling 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>lpvInBuffer</i>, <i>lpvOutBuffer</i>, <i>lpcbBytesReturned</i>, <i>lpOverlapped</i>, or <i>lpCompletionRoutine</i> parameter is not totally contained in a valid part of the user address space, or the <i>cbInBuffer</i> or <i>cbOutBuffer</i> parameter is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>dwIoControlCode</i> parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINPROGRESS</a></b></dt>
</dl>
</td>
<td width="60%">
The function is invoked when a callback is in progress.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOTSOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The descriptor <i>s</i> is not a socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEOPNOTSUPP</a></b></dt>
</dl>
</td>
<td width="60%">
The specified IOCTL command cannot be realized. (For example, the 
<a href="/windows/desktop/api/qos/ns-qos-flowspec">FLOWSPEC</a> structures specified in <b>SIO_SET_QOS</b> or <b>SIO_SET_GROUP_QOS</b> cannot be satisfied.)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEWOULDBLOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The socket is marked as non-blocking and the requested operation would block.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOPROTOOPT</a></b></dt>
</dl>
</td>
<td width="60%">
The socket option is not supported on the specified protocol. For example, an attempt to use the <b>SIO_GET_BROADCAST_ADDRESS</b> IOCTL was made on an IPv6 socket or an attempt to use the TCP <b>SIO_KEEPALIVE_VALS</b> IOCTL was made on a datagram socket.

</td>
</tr>
</table>

## -remarks

The 
<b>WSAIoctl</b> function is used to set or retrieve operating parameters associated with the socket, the transport protocol, or the communications subsystem.

If both <i>lpOverlapped</i> and <i>lpCompletionRoutine</i> are <b>NULL</b>, the socket in this function will be treated as a non-overlapped socket. For a non-overlapped socket, <i>lpOverlapped</i> and <i>lpCompletionRoutine</i> parameters are ignored, which causes the function to behave like the standard 
<a href="/windows/desktop/api/winsock/nf-winsock-ioctlsocket">ioctlsocket</a> function except that  the function can block if socket <i>s</i> is in blocking mode. If socket <i>s</i> is in non-blocking mode, this function can return WSAEWOULDBLOCK when the specified operation cannot be finished immediately. In this case, the application may change the socket to blocking mode and reissue the request or wait for the corresponding network event (such as FD_ROUTING_INTERFACE_CHANGE or FD_ADDRESS_LIST_CHANGE in the case of <b>SIO_ROUTING_INTERFACE_CHANGE</b> or <b>SIO_ADDRESS_LIST_CHANGE</b>) using a Windows message (using 
<a href="/windows/desktop/api/winsock/nf-winsock-wsaasyncselect">WSAAsyncSelect</a>)-based or event (using 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaeventselect">WSAEventSelect</a>)-based notification mechanism.

For overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time. The <b>DWORD</b> value pointed to by the <i>lpcbBytesReturned</i> parameter that is returned may be ignored. The final completion status and bytes returned can be retrieved when the appropriate completion method is signaled when the operation 
       has completed.  
       

Any IOCTL may block indefinitely, depending on the service provider's implementation. If the application cannot tolerate blocking in a 
<b>WSAIoctl</b> call, overlapped I/O would be advised for IOCTLs that are especially likely to block including:

<b>SIO_ADDRESS_LIST_CHANGE</b>

<b>SIO_FINDROUTE</b>

<b>SIO_FLUSH</b>

<b>SIO_GET_QOS</b>

<b>SIO_GET_GROUP_QOS</b>

<b>SIO_ROUTING_INTERFACE_CHANGE</b>

<b>SIO_SET_QOS</b>

<b>SIO_SET_GROUP_QOS</b>

Some protocol-specific IOCTLs may also be especially likely to block. Check the relevant protocol-specific annex for any available information.

The prototype for the completion routine pointed to by the <i>lpCompletionRoutine</i> parameter is as follows:


```cpp
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")


void CALLBACK CompletionRoutine (
  IN DWORD dwError,
  IN DWORD cbTransferred,
  IN LPWSAOVERLAPPED lpOverlapped,
  IN DWORD dwFlags 
);

```


The CompletionRoutine is a placeholder for an application-supplied function name. The <i>dwError</i> parameter specifies the completion status for the overlapped operation as indicated by <i>lpOverlapped</i> parameter. The  <i>cbTransferred</i> parameter specifies the number of bytes received. The <i>dwFlags</i> parameter is not used  for this IOCTL. The completion routine does not return a value.

It is possible to adopt an encoding scheme that preserves the currently defined 
<a href="/windows/desktop/api/winsock/nf-winsock-ioctlsocket">ioctlsocket</a> opcodes while providing a convenient way to partition the opcode identifier space in as much as the <i>dwIoControlCode</i> parameter is now a 32-bit entity. The <i>dwIoControlCode</i> parameter is built to allow for protocol and vendor independence when adding new control codes while retaining backward compatibility with the Windows Sockets 1.1 and Unix control codes. The <i>dwIoControlCode</i> parameter has the following form.

<table>
<tr>
<th>I</th>
<th>O</th>
<th>V</th>
<th>T</th>
<th>Vendor/address family</th>
<th>Code</th>
</tr>
<tr>
<td>3</td>
<td>3</td>
<td>2</td>
<td>2 2</td>
<td>2 2 2 2 2 2 2 1 1 1 1</td>
<td>1 1 1 1 1 1 </td>
</tr>
<tr>
<td>1</td>
<td>0</td>
<td>9</td>
<td>8 7</td>
<td>6 5 4 3 2 1 0 9 8 7 6</td>
<td>5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>   The bits in <i>dwIoControlCode</i> parameter displayed in the table must be read vertically from top to bottom by column. So the left-most bit is bit 31, the next bit is bit 30, and the right-most bit is bit 0. </div>
<div> </div>
I is set if the input buffer is valid for the code, as with <b>IOC_IN</b>.

O is set if the output buffer is valid for the code, as with <b>IOC_OUT</b>. Control codes using both input and output buffers set both I and O.

V is set if there are no parameters for the code, as with <b>IOC_VOID</b>.

T is a 2-bit quantity that defines the type of the IOCTL. The following values are defined:

0 The IOCTL is a standard Unix IOCTL code, as with <b>FIONREAD</b> and <b>FIONBIO</b>.

1 The IOCTL is a generic Windows Sockets 2 IOCTL code. New IOCTL codes defined for Windows Sockets 2 will have T == 1.

2 The IOCTL applies only to a specific address family.

3 The IOCTL applies only to a specific vendor's provider, as with <b>IOC_VENDOR</b>. This type allows companies to be assigned a vendor number that appears in the <b>Vendor/Address family</b> parameter. Then, the vendor can define new IOCTLs specific to that vendor without having to register the IOCTL with a clearinghouse, thereby providing vendor flexibility and privacy.

<b>Vendor/Address family</b> An 11-bit quantity that defines the vendor who owns the code (if T == 3) or that contains the address family to which the code applies (if T == 2). If this is a Unix IOCTL code (T == 0) then this parameter has the same value as the code on Unix. If this is a generic Windows Sockets 2 IOCTL (T == 1) then this parameter can be used as an extension of the code parameter to provide additional code values.

<b>Code</b> The 16-bit quantity that contains the specific IOCTL code for the operation.

The following Unix IOCTL codes (commands) are supported.



The following Windows Sockets 2 commands are supported.



If an overlapped operation completes immediately, 
<b>WSAIoctl</b> returns a value of zero and the <i>lpcbBytesReturned</i> parameter is updated with the number of bytes in the output buffer. If the overlapped operation is successfully initiated and will complete later, this function returns SOCKET_ERROR and indicates error code 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_IO_PENDING</a>. In this case, <i>lpcbBytesReturned</i> is not updated. When the overlapped operation completes the amount of data in the output buffer is indicated either through the <i>cbTransferred</i> parameter in the completion routine (if specified), or through the <i>lpcbTransfer</i> parameter in 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult">WSAGetOverlappedResult</a>.

When called with an overlapped socket, the <i>lpOverlapped</i> parameter must be valid for the duration of the overlapped operation. The <i>lpOverlapped</i> parameter contains the address of a 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped">WSAOVERLAPPED</a> structure.

If the <i>lpCompletionRoutine</i> parameter is <b>NULL</b>, the <i>hEvent</i> parameter of <i>lpOverlapped</i> is signaled when the overlapped operation completes if it contains a valid event object handle. An application can use 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsawaitformultipleevents">WSAWaitForMultipleEvents</a> or 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult">WSAGetOverlappedResult</a> to wait or poll on the event object.

<div class="alert"><b>Note</b>  All I/O initiated by a given thread is canceled when that thread exits. For overlapped sockets, pending asynchronous operations can fail if the thread is closed before the  operations complete. See <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread">ExitThread</a> for more information.</div>
<div> </div>
If <i>lpCompletionRoutine</i> is not <b>NULL</b>, the <i>hEvent</i> parameter is ignored and can be used by the application to pass context information to the completion routine. A caller that passes a non-<b>NULL</b> <i>lpCompletionRoutine</i> and later calls 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult">WSAGetOverlappedResult</a> for the same overlapped I/O request may not set the <i>fWait</i> parameter for that invocation of 
<b>WSAGetOverlappedResult</b> to <b>TRUE</b>. In this case, the usage of the <i>hEvent</i> parameter is undefined, and attempting to wait on the <i>hEvent</i> parameter would produce unpredictable results.

The prototype of the completion routine is as follows:


```cpp

void CALLBACK CompletionRoutine(
  IN DWORD dwError, 
  IN DWORD cbTransferred, 
  IN LPWSAOVERLAPPED lpOverlapped, 
  IN DWORD dwFlags 
);

```


This <b>CompletionRoutine</b> is a placeholder for an application-defined or library-defined function. The completion routine is invoked only if the thread is in an alertable state. To put a thread into an alertable state, use  the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsawaitformultipleevents">WSAWaitForMultipleEvents</a>, <a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex">WaitForSingleObjectEx</a>, or <a href="/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex">WaitForMultipleObjectsEx</a> function with the <i>fAlertable</i> or <i>bAlertable</i> parameter set to <b>TRUE</b>.

The <i>dwError</i> parameter of <b>CompletionRoutine</b>     specifies the completion status for the overlapped operation as indicated by <i>lpOverlapped</i>. The <i>cbTransferred</i> parameter specifies the number of bytes returned. Currently, no flag values are defined and <i>dwFlags</i> will be zero. The <b>CompletionRoutine</b> function does not return a value.

Returning from this function allows invocation of another pending completion routine for this socket. The completion routines can be called in any order, not necessarily in the same order the overlapped operations are completed.

<h3><a id="Compatibility"></a><a id="compatibility"></a><a id="COMPATIBILITY"></a>Compatibility</h3>
The IOCTL codes with T == 0 are a subset of the IOCTL codes used in Berkeley sockets. In particular, there is no command that is equivalent to <b>FIOASYNC</b>.

<div class="alert"><b>Note</b>  Some IOCTL codes require additional header files. For example, use of the <b>SIO_RCVALL</b> IOCTL requires the Mstcpip.h header file.</div>
<div> </div>
<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/WinSock/sol-socket-socket-options">SOL_SOCKET Socket Options</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasocketa">WSASocket</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>



<a href="/windows/desktop/api/winsock/nf-winsock-getsockopt">getsockopt</a>



<a href="/windows/desktop/api/winsock/nf-winsock-ioctlsocket">ioctlsocket</a>



<a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-socket">socket</a>