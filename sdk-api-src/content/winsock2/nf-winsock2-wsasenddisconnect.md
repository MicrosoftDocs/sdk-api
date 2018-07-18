---
UID: NF:winsock2.WSASendDisconnect
title: WSASendDisconnect function
author: windows-sdk-content
description: The WSASendDisconnect function initiates termination of the connection for the socket and sends disconnect data.
old-location: winsock\wsasenddisconnect_2.htm
old-project: winsock
ms.assetid: c05fc719-e35a-4194-ac01-a294b19ccce9
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: WSASendDisconnect, WSASendDisconnect function [Winsock], _win32_wsasenddisconnect_2, winsock.wsasenddisconnect_2, winsock2/WSASendDisconnect
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winsock2.h
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
 - WSASendDisconnect
product: Windows
targetos: Windows
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSASendDisconnect function


## -description



			The 
<b>WSASendDisconnect</b> function initiates termination of the connection for the socket and sends disconnect data.


## -parameters




### -param s [in]

Descriptor identifying a socket.


### -param lpOutboundDisconnectData [in]

A pointer to the outgoing disconnect data.


## -returns



If no error occurs, 
<b>WSASendDisconnect</b> returns zero. Otherwise, a value of SOCKET_ERROR is returned, and a specific error code can be retrieved by calling 
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
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAENOPROTOOPT</a></b></dt>
</dl>
</td>
<td width="60%">
The parameter <i>lpOutboundDisconnectData</i> is not <b>NULL</b>, and the disconnect data is not supported by the service provider.

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
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAENOTCONN</a></b></dt>
</dl>
</td>
<td width="60%">
The socket is not connected (connection-oriented sockets only).

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
The <i>lpOutboundDisconnectData</i> parameter is not completely contained in a valid part of the user address space.

</td>
</tr>
</table>
 




## -remarks



The 
<b>WSASendDisconnect</b> function is used on connection-oriented sockets to disable transmission and to initiate termination of the connection along with the transmission of disconnect data, if any. This is equivalent to a shutdown (SD_SEND), except that 
<b>WSASendDisconnect</b> also allows sending disconnect data (in protocols that support it).

After this function has been successfully issued, subsequent sends are disallowed.

The <i>lpOutboundDisconnectData</i> parameter, if not <b>NULL</b>, points to a buffer containing the outgoing disconnect data to be sent to the remote party for retrieval by using 
<a href="https://msdn.microsoft.com/33e0fb8e-3ece-427f-b3ef-43a0f5cf0cc8">WSARecvDisconnect</a>.

<div class="alert"><b>Note</b>  The native implementation of TCP/IP on Windows does not support disconnect data. Disconnect data is only supported with Windows Sockets providers that have the XP1_DISCONNECT_DATA flag in their 
<a href="https://msdn.microsoft.com/758c5553-056f-4ea5-a851-30ef641ffb14">WSAPROTOCOL_INFO</a> structure. Use the 
<a href="https://msdn.microsoft.com/928b6937-41a3-4268-a3bc-14c9e04870e4">WSAEnumProtocols</a> function to obtain 
<b>WSAPROTOCOL_INFO</b> structures for all installed providers.</div>
<div> </div>
The 
<b>WSASendDisconnect</b> function does not close the socket, and resources attached to the socket will not be freed until 
<a href="https://msdn.microsoft.com/2f357aa8-389b-4c92-8a9f-289e048cc41c">closesocket</a> is invoked.

The 
<b>WSASendDisconnect</b> function does not block regardless of the SO_LINGER setting on the socket.

An application should not rely on being able to reuse a socket after calling 
<b>WSASendDisconnect</b>. In particular, a Windows Sockets provider is not required to support the use of 
<a href="https://msdn.microsoft.com/13468139-dc03-45bd-850c-7ac2dbcb6e60">connect</a>/<a href="https://msdn.microsoft.com/3b32cc6e-3df7-4104-a0d4-317fd445c7b2">WSAConnect</a> on such a socket.

<div class="alert"><b>Note</b>  When issuing a blocking Winsock call such as <b>WSASendDisconnect</b>,  Winsock may need to wait for a network event before the call can complete. Winsock performs an alertable wait in this situation, which can be interrupted by an asynchronous procedure call (APC) scheduled on the same thread. Issuing another blocking Winsock call inside an APC that interrupted an ongoing blocking Winsock call on the same thread will lead to undefined behavior, and must never be attempted by Winsock clients. </div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>



<a href="https://msdn.microsoft.com/13468139-dc03-45bd-850c-7ac2dbcb6e60">connect</a>



<a href="https://msdn.microsoft.com/6bf6e6c4-6268-479c-86a6-52e90cf317db">socket</a>
 

 

