---
UID: NF:winsock2.WSARecvDisconnect
title: WSARecvDisconnect function (winsock2.h)
description: The WSARecvDisconnect function terminates reception on a socket, and retrieves the disconnect data if the socket is connection oriented.
helpviewer_keywords: ["WSARecvDisconnect","WSARecvDisconnect function [Winsock]","_win32_wsarecvdisconnect_2","winsock.wsarecvdisconnect_2","winsock2/WSARecvDisconnect"]
old-location: winsock\wsarecvdisconnect_2.htm
tech.root: WinSock
ms.assetid: 33e0fb8e-3ece-427f-b3ef-43a0f5cf0cc8
ms.date: 12/05/2018
ms.keywords: WSARecvDisconnect, WSARecvDisconnect function [Winsock], _win32_wsarecvdisconnect_2, winsock.wsarecvdisconnect_2, winsock2/WSARecvDisconnect
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
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WSARecvDisconnect
 - winsock2/WSARecvDisconnect
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
 - WSARecvDisconnect
---

# WSARecvDisconnect function


## -description

The 
<b>WSARecvDisconnect</b> function terminates reception on a socket, and retrieves the disconnect data if the socket is connection oriented.

## -parameters

### -param s [in]

A descriptor identifying a socket.

### -param lpInboundDisconnectData [out]

A pointer to the incoming disconnect data.

## -returns

If no error occurs, 
<b>WSARecvDisconnect</b> returns zero. Otherwise, a value of SOCKET_ERROR is returned, and a specific error code can be retrieved by calling 
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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The buffer referenced by the parameter <i>lpInboundDisconnectData</i> is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOPROTOOPT</a></b></dt>
</dl>
</td>
<td width="60%">
The disconnect data is not supported by the indicated protocol family. Note that implementations of TCP/IP that do not support disconnect data are not required to return the WSAENOPROTOOPT error code. See the remarks section for information about the Microsoft implementation of TCP/IP.

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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOTCONN</a></b></dt>
</dl>
</td>
<td width="60%">
The socket is not connected (connection-oriented sockets only).

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
</table>

## -remarks

The 
<b>WSARecvDisconnect</b> function is used on connection-oriented sockets to disable reception and retrieve any incoming disconnect data from the remote party. This is equivalent to a shutdown (SD_RECEIVE), except that 
<b>WSARecvDisconnect</b> also allows receipt of disconnect data (in protocols that support it).

After this function has been successfully issued, subsequent receives on the socket will be disallowed. Calling 
<b>WSARecvDisconnect</b> has no effect on the lower protocol layers. For TCP sockets, if there is still data queued on the socket waiting to be received, or data arrives subsequently, the connection is reset, since the data cannot be delivered to the user. For UDP, incoming datagrams are accepted and queued. In no case will an ICMP error packet be generated.

<div class="alert"><b>Note</b>  The native implementation of TCP/IP on Windows does not support disconnect data. Disconnect data is only supported with Windows Sockets providers that have the XP1_DISCONNECT_DATA flag in their 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structure. Use the 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumprotocolsa">WSAEnumProtocols</a> function to obtain 
<b>WSAPROTOCOL_INFO</b> structures for all installed providers.</div>
<div> </div>
To successfully receive incoming disconnect data, an application must use other mechanisms to determine that the circuit has been closed. For example, an application needs to receive an FD_CLOSE notification, to receive a zero return value, or to receive a 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEDISCON</a> or 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAECONNRESET</a> error code from 
<a href="/windows/desktop/api/winsock/nf-winsock-recv">recv</a>/<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecv">WSARecv</a>.

The 
<b>WSARecvDisconnect</b> function does not close the socket, and resources attached to the socket will not be freed until 
<a href="/windows/desktop/api/winsock/nf-winsock-closesocket">closesocket</a> is invoked.

The 
<b>WSARecvDisconnect</b> function does not block regardless of the SO_LINGER setting on the socket.

An application should not rely on being able to reuse a socket after it has been disconnected using 
<b>WSARecvDisconnect</b>. In particular, a Windows Sockets provider is not required to support the use of 
<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a> or 
				<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnect">WSAConnect</a> on such a socket.

<div class="alert"><b>Note</b>  When issuing a blocking Winsock call such as <b>WSARecvDisconnect</b>,  Winsock may need to wait for a network event before the call can complete. Winsock performs an alertable wait in this situation, which can be interrupted by an asynchronous procedure call (APC) scheduled on the same thread. Issuing another blocking Winsock call inside an APC that interrupted an ongoing blocking Winsock call on the same thread will lead to undefined behavior, and must never be attempted by Winsock clients. </div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnect">WSAConnect</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumprotocolsa">WSAEnumProtocols</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>



<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecv">WSARecv</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>



<a href="/windows/desktop/api/winsock/nf-winsock-closesocket">closesocket</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-socket">socket</a>