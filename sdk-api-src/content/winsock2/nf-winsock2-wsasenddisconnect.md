---
UID: NF:winsock2.WSASendDisconnect
title: WSASendDisconnect function (winsock2.h)
description: The WSASendDisconnect function initiates termination of the connection for the socket and sends disconnect data.
helpviewer_keywords: ["WSASendDisconnect","WSASendDisconnect function [Winsock]","_win32_wsasenddisconnect_2","winsock.wsasenddisconnect_2","winsock2/WSASendDisconnect"]
old-location: winsock\wsasenddisconnect_2.htm
tech.root: WinSock
ms.assetid: c05fc719-e35a-4194-ac01-a294b19ccce9
ms.date: 12/05/2018
ms.keywords: WSASendDisconnect, WSASendDisconnect function [Winsock], _win32_wsasenddisconnect_2, winsock.wsasenddisconnect_2, winsock2/WSASendDisconnect
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
 - WSASendDisconnect
 - winsock2/WSASendDisconnect
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
 - WSASendDisconnect
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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOPROTOOPT</a></b></dt>
</dl>
</td>
<td width="60%">
The parameter <i>lpOutboundDisconnectData</i> is not <b>NULL</b>, and the disconnect data is not supported by the service provider.

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
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
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
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecvdisconnect">WSARecvDisconnect</a>.

<div class="alert"><b>Note</b>  The native implementation of TCP/IP on Windows does not support disconnect data. Disconnect data is only supported with Windows Sockets providers that have the XP1_DISCONNECT_DATA flag in their 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structure. Use the 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumprotocolsa">WSAEnumProtocols</a> function to obtain 
<b>WSAPROTOCOL_INFO</b> structures for all installed providers.</div>
<div> </div>
The 
<b>WSASendDisconnect</b> function does not close the socket, and resources attached to the socket will not be freed until 
<a href="/windows/desktop/api/winsock/nf-winsock-closesocket">closesocket</a> is invoked.

The 
<b>WSASendDisconnect</b> function does not block regardless of the SO_LINGER setting on the socket.

An application should not rely on being able to reuse a socket after calling 
<b>WSASendDisconnect</b>. In particular, a Windows Sockets provider is not required to support the use of 
<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a>/<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnect">WSAConnect</a> on such a socket.

<div class="alert"><b>Note</b>  When issuing a blocking Winsock call such as <b>WSASendDisconnect</b>,  Winsock may need to wait for a network event before the call can complete. Winsock performs an alertable wait in this situation, which can be interrupted by an asynchronous procedure call (APC) scheduled on the same thread. Issuing another blocking Winsock call inside an APC that interrupted an ongoing blocking Winsock call on the same thread will lead to undefined behavior, and must never be attempted by Winsock clients. </div>
<div> </div>

## -see-also

<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-socket">socket</a>