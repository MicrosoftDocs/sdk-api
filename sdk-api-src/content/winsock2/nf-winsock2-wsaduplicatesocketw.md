---
UID: NF:winsock2.WSADuplicateSocketW
title: WSADuplicateSocketW function
author: windows-sdk-content
description: The WSADuplicateSocket function returns a WSAPROTOCOL_INFO structure that can be used to create a new socket descriptor for a shared socket. The WSADuplicateSocket function cannot be used on a QOS-enabled socket.
old-location: winsock\wsaduplicatesocket_2.htm
old-project: WinSock
ms.assetid: d4028461-bfa6-4074-9460-5d1371790d41
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: WSADuplicateSocket, WSADuplicateSocket function [Winsock], WSADuplicateSocketA, WSADuplicateSocketW, _win32_wsaduplicatesocket_2, winsock.wsaduplicatesocket_2, winsock2/WSADuplicateSocket, winsock2/WSADuplicateSocketA, winsock2/WSADuplicateSocketW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winsock2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WSADuplicateSocketW (Unicode) and WSADuplicateSocketA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSAECOMPARATOR, *PWSAECOMPARATOR, *LPWSAECOMPARATOR
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
product: Windows
targetos: Windows
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSADuplicateSocketW function


## -description



			The 
<b>WSADuplicateSocket</b> function returns a 
<a href="https://msdn.microsoft.com/758c5553-056f-4ea5-a851-30ef641ffb14">WSAPROTOCOL_INFO</a> structure that can be used to create a new socket descriptor for a shared socket. The 
<b>WSADuplicateSocket</b> function cannot be used on a QOS-enabled socket.


## -parameters




### -param s [in]

Descriptor identifying the local socket.


### -param dwProcessId [in]

Process identifier of the target process in which the duplicated socket will be used.


### -param lpProtocolInfo [out]

Pointer to a buffer, allocated by the client, that is large enough to contain a 
<a href="https://msdn.microsoft.com/758c5553-056f-4ea5-a851-30ef641ffb14">WSAPROTOCOL_INFO</a> structure. The service provider copies the protocol information structure contents to this buffer.


## -returns



If no error occurs, 
<b>WSADuplicateSocket</b> returns zero. Otherwise, a value of SOCKET_ERROR is returned, and a specific error code can be retrieved by calling 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSANOTINITIALISED</a></b></dt>
</dl>
</td>
<td width="60%">
A successful 
<a href="https://msdn.microsoft.com/08299592-867c-491d-9769-d16602133659">WSAStartup</a> call must occur before using this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAENETDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
The network subsystem has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
Indicates that one of the specified parameters was invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAEINPROGRESS</a></b></dt>
</dl>
</td>
<td width="60%">
A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAEMFILE</a></b></dt>
</dl>
</td>
<td width="60%">
No more socket descriptors are available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAENOBUFS</a></b></dt>
</dl>
</td>
<td width="60%">
No buffer space is available. The socket cannot be created.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAENOTSOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The descriptor is not a socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAEFAULT</a></b></dt>
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
<a href="https://msdn.microsoft.com/758c5553-056f-4ea5-a851-30ef641ffb14">WSAPROTOCOL_INFO</a> structure. It uses some interprocess communications (IPC) mechanism to pass the contents of this structure to a target process, which in turn uses it in a call to 
<a href="https://msdn.microsoft.com/dcf2e543-de54-43d9-9e45-4cb935da3548">WSASocket</a> to obtain a descriptor for the duplicated socket. The special 
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
<a href="https://msdn.microsoft.com/dcf2e543-de54-43d9-9e45-4cb935da3548">WSASocket</a>, 
<a href="https://msdn.microsoft.com/3b32cc6e-3df7-4104-a0d4-317fd445c7b2">WSAConnect</a>
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
<a href="https://msdn.microsoft.com/758c5553-056f-4ea5-a851-30ef641ffb14">WSAPROTOCOL_INFO</a> structure</td>
<td></td>
<td></td>
</tr>
<tr>
<td>6) Send 
<a href="https://msdn.microsoft.com/758c5553-056f-4ea5-a851-30ef641ffb14">WSAPROTOCOL_INFO</a> structure to target</td>
<td></td>
<td></td>
</tr>
<tr>
<td></td>
<td>==&gt;</td>
<td>7) Receive 
<a href="https://msdn.microsoft.com/758c5553-056f-4ea5-a851-30ef641ffb14">WSAPROTOCOL_INFO</a> structure</td>
</tr>
<tr>
<td></td>
<td></td>
<td>8) Call 
<a href="https://msdn.microsoft.com/dcf2e543-de54-43d9-9e45-4cb935da3548">WSASocket</a> to create shared socket descriptor.</td>
</tr>
<tr>
<td></td>
<td></td>
<td>9) Use shared socket for data exchange</td>
</tr>
<tr>
<td>10) 
<a href="https://msdn.microsoft.com/2f357aa8-389b-4c92-8a9f-289e048cc41c">closesocket</a>
</td>
<td>&lt;==</td>
<td></td>
</tr>
</table>
 

The descriptors that reference a shared socket can be used independently for I/O. However, the Windows Sockets interface does not implement any type of access control, so it is up to the processes involved to coordinate their operations on a shared socket. Shared sockets are typically used to having one process that is responsible for creating sockets and establishing connections, and other processes that are responsible for information exchange.

All of the state information associated with a socket is held in common across all the descriptors because the socket descriptors are duplicated and not the actual socket. For example, a 
<a href="https://msdn.microsoft.com/3a6960c9-0c04-4403-aee1-ce250459dc30">setsockopt</a> operation performed using one descriptor is subsequently visible using a 
<a href="https://msdn.microsoft.com/25bc511d-7a9f-41c1-8983-1af1e3f8bf2d">getsockopt</a> from any or all descriptors. Both the source process and the destination process should pass the same flags to their respective <a href="https://msdn.microsoft.com/dcf2e543-de54-43d9-9e45-4cb935da3548">WSASocket</a> function calls. If the source process uses the <a href="https://msdn.microsoft.com/6bf6e6c4-6268-479c-86a6-52e90cf317db">socket</a> function to create the socket, the destination process must pass the <b>WSA_FLAG_OVERLAPPED</b> flag to its <b>WSASocket</b> function call. A process can call 
<a href="https://msdn.microsoft.com/2f357aa8-389b-4c92-8a9f-289e048cc41c">closesocket</a> on a duplicated socket and the descriptor will become deallocated. The underlying socket, however, will remain open until 
<b>closesocket</b> is called by the last remaining descriptor.

Notification on shared sockets is subject to the usual constraints of 
<a href="https://msdn.microsoft.com/a4d3f599-358c-4a94-91eb-7e1c80244250">WSAAsyncSelect</a> and 
<a href="https://msdn.microsoft.com/f98a71e4-47fb-47a4-b37e-e4cc801a8f98">WSAEventSelect</a>. Issuing either of these calls using any of the shared descriptors cancels any previous event registration for the socket, regardless of which descriptor was used to make that registration. Thus, a shared socket cannot deliver FD_READ events to process A and FD_WRITE events to process B. For situations when such tight coordination is required, developers would be advised to use threads instead of separate processes.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: The  <b>WSADuplicateSocketW</b> function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<a href="https://msdn.microsoft.com/dcf2e543-de54-43d9-9e45-4cb935da3548">WSASocket</a>



<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>
 

 

