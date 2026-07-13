---
UID: NF:winsock2.WSADuplicateSocketA
title: WSADuplicateSocketA function (winsock2.h)
description: The WSADuplicateSocket function returns a WSAPROTOCOL_INFO structure that can be used to create a new socket descriptor for a shared socket. The WSADuplicateSocket function cannot be used on a QOS-enabled socket. (ANSI)
helpviewer_keywords: ["WSADuplicateSocketA", "winsock2/WSADuplicateSocketA"]
old-location: winsock\wsaduplicatesocket_2.htm
tech.root: WinSock
ms.assetid: d4028461-bfa6-4074-9460-5d1371790d41
ms.date: 12/05/2018
ms.keywords: WSADuplicateSocket, WSADuplicateSocket function [Winsock], WSADuplicateSocketA, WSADuplicateSocketW, _win32_wsaduplicatesocket_2, winsock.wsaduplicatesocket_2, winsock2/WSADuplicateSocket, winsock2/WSADuplicateSocketA, winsock2/WSADuplicateSocketW
req.header: winsock2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WSADuplicateSocketW (Unicode) and WSADuplicateSocketA (ANSI)
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
 - WSADuplicateSocketA
 - winsock2/WSADuplicateSocketA
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
 - WSADuplicateSocket
 - WSADuplicateSocketA
 - WSADuplicateSocketW
---

# WSADuplicateSocketA function


## -description

The 
<b>WSADuplicateSocket</b> function returns a 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structure that can be used to create a new socket descriptor for a shared socket. The 
<b>WSADuplicateSocket</b> function cannot be used on a QOS-enabled socket.

## -parameters

### -param s [in]

Descriptor identifying the local socket.

### -param dwProcessId [in]

Process identifier of the target process in which the duplicated socket will be used.

### -param lpProtocolInfo [out]

Pointer to a buffer, allocated by the client, that is large enough to contain a 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structure. The service provider copies the protocol information structure contents to this buffer.

## -returns

If no error occurs, 
<b>WSADuplicateSocket</b> returns zero. Otherwise, a value of SOCKET_ERROR is returned, and a specific error code can be retrieved by calling 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANOTINITIALISED</a></b></dt>
</dl>
</td>
<td width="60%">
A successful 
<a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a> call must occur before using this function.

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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
Indicates that one of the specified parameters was invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINPROGRESS</a></b></dt>
</dl>
</td>
<td width="60%">
A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEMFILE</a></b></dt>
</dl>
</td>
<td width="60%">
No more socket descriptors are available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOBUFS</a></b></dt>
</dl>
</td>
<td width="60%">
No buffer space is available. The socket cannot be created.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOTSOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The descriptor is not a socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>lpProtocolInfo</i> parameter is not a valid part of the user address space.

</td>
</tr>
</table>

## -remarks

The 
<b>WSADuplicateSocket</b> function is used to enable socket sharing between processes. A source process calls 
<b>WSADuplicateSocket</b> to obtain a special 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structure. It uses some interprocess communications (IPC) mechanism to pass the contents of this structure to a target process, which in turn uses it in a call to 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasocketa">WSASocket</a> to obtain a descriptor for the duplicated socket. The special 
<b>WSAPROTOCOL_INFO</b> structure can only be used once by the target process.

Sockets can be shared among threads in a given process without using the 
<b>WSADuplicateSocket</b> function because a socket descriptor is valid in all threads of a process.

One possible scenario for establishing and handing off a shared socket is illustrated in the following table.

<table>
<tr>
<th>Source process</th>
<th>IPC</th>
<th>Destination process</th>
</tr>
<tr>
<td>1) 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasocketa">WSASocket</a>, 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnect">WSAConnect</a>
</td>
<td></td>
<td></td>
</tr>
<tr>
<td>2) Request target process identifier</td>
<td>==&gt;</td>
<td></td>
</tr>
<tr>
<td></td>
<td></td>
<td>3) Receive process identifier request and respond</td>
</tr>
<tr>
<td>4) Receive process identifier</td>
<td>&lt;==</td>
<td></td>
</tr>
<tr>
<td>5) Call 
<b>WSADuplicateSocket</b> to get a special 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structure</td>
<td></td>
<td></td>
</tr>
<tr>
<td>6) Send 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structure to target</td>
<td></td>
<td></td>
</tr>
<tr>
<td></td>
<td>==&gt;</td>
<td>7) Receive 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structure</td>
</tr>
<tr>
<td></td>
<td></td>
<td>8) Call 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasocketa">WSASocket</a> to create shared socket descriptor.</td>
</tr>
<tr>
<td></td>
<td></td>
<td>9) Use shared socket for data exchange</td>
</tr>
<tr>
<td>10) 
<a href="/windows/desktop/api/winsock/nf-winsock-closesocket">closesocket</a>
</td>
<td>&lt;==</td>
<td></td>
</tr>
</table>
 

The descriptors that reference a shared socket can be used independently for I/O. However, the Windows Sockets interface does not implement any type of access control, so it is up to the processes involved to coordinate their operations on a shared socket. Shared sockets are typically used to having one process that is responsible for creating sockets and establishing connections, and other processes that are responsible for information exchange.

All of the state information associated with a socket is held in common across all the descriptors because the socket descriptors are duplicated and not the actual socket. For example, a 
<a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a> operation performed using one descriptor is subsequently visible using a 
<a href="/windows/desktop/api/winsock/nf-winsock-getsockopt">getsockopt</a> from any or all descriptors. Both the source process and the destination process should pass the same flags to their respective <a href="/windows/desktop/api/winsock2/nf-winsock2-wsasocketa">WSASocket</a> function calls. If the source process uses the <a href="/windows/desktop/api/winsock2/nf-winsock2-socket">socket</a> function to create the socket, the destination process must pass the <b>WSA_FLAG_OVERLAPPED</b> flag to its <b>WSASocket</b> function call. A process can call 
<a href="/windows/desktop/api/winsock/nf-winsock-closesocket">closesocket</a> on a duplicated socket and the descriptor will become deallocated. The underlying socket, however, will remain open until 
<b>closesocket</b> is called by the last remaining descriptor.

Notification on shared sockets is subject to the usual constraints of 
<a href="/windows/desktop/api/winsock/nf-winsock-wsaasyncselect">WSAAsyncSelect</a> and 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaeventselect">WSAEventSelect</a>. Issuing either of these calls using any of the shared descriptors cancels any previous event registration for the socket, regardless of which descriptor was used to make that registration. Thus, a shared socket cannot deliver FD_READ events to process A and FD_WRITE events to process B. For situations when such tight coordination is required, developers would be advised to use threads instead of separate processes.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: The  <b>WSADuplicateSocketW</b> function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.





> [!NOTE]
> The winsock2.h header defines WSADuplicateSocket as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasocketa">WSASocket</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>
