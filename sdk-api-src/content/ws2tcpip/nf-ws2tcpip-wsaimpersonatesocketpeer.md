---
UID: NF:ws2tcpip.WSAImpersonateSocketPeer
title: WSAImpersonateSocketPeer function (ws2tcpip.h)
description: Used to impersonate the security principal corresponding to a socket peer in order to perform application-level authorization.
helpviewer_keywords: ["WSAImpersonateSocketPeer","WSAImpersonateSocketPeer function [Winsock]","winsock.wsaimpersonatesocketpeer","ws2tcpip/WSAImpersonateSocketPeer"]
old-location: winsock\wsaimpersonatesocketpeer.htm
tech.root: WinSock
ms.assetid: 8dd2c0dd-ca1d-40b8-8e58-a980e67b6941
ms.date: 12/05/2018
ms.keywords: WSAImpersonateSocketPeer, WSAImpersonateSocketPeer function [Winsock], winsock.wsaimpersonatesocketpeer, ws2tcpip/WSAImpersonateSocketPeer
req.header: ws2tcpip.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WSAImpersonateSocketPeer
 - ws2tcpip/WSAImpersonateSocketPeer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Fwpuclnt.dll
api_name:
 - WSAImpersonateSocketPeer
---

# WSAImpersonateSocketPeer function


## -description

The <b>WSAImpersonateSocketPeer</b> function is used to impersonate the security principal corresponding to a socket peer in order to perform application-level authorization.

## -parameters

### -param Socket [in]

Identifies the application socket.

### -param PeerAddr [in, optional]

The IP address of the peer to be impersonated.  For connection-oriented sockets, the connected socket uniquely identifies a peer.  In this case, this parameter is ignored.

### -param PeerAddrLen [in]

The size, in bytes, of the <i>PeerAddress</i> parameter.

## -returns

If the function succeeds, the return value is 0.  Otherwise, a value of <b>SOCKET_ERROR</b> is returned, and a specific error code can be retrieved by calling 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>. 

Some possible error codes are listed below.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The system detected an invalid address pointer in attempting to use a pointer argument of a call. This error is returned if the <i>PeerAddr</i> parameter was a <b>NULL</b> pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEAFNOSUPPORT</a></b></dt>
</dl>
</td>
<td width="60%">
The specified address family is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEMSGSIZE</a></b></dt>
</dl>
</td>
<td width="60%">
A buffer passed was too small. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOTSOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The descriptor passed in the <i>Socket</i> parameter is not a valid socket.

</td>
</tr>
</table>

## -remarks

The <b>WSAImpersonateSocketPeer</b> function provides an application the ability to impersonate the security principal corresponding to a socket peer in order to perform application-level authorization. If peer user (impersonation) token is available then it will be used for impersonation, otherwise the peer computer token will be used. The <b>WSAImpersonateSocketPeer</b> function can be called only for blocking, non-overlapped sockets. After performing any authorization checks, an application must call the <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsarevertimpersonation">WSARevertImpersonation</a> function to terminate the impersonation.

For connection-oriented sockets, the <b>WSAImpersonateSocketPeer</b> function should be called after a connection is established. For a server application using connection-oriented sockets, the <b>WSAImpersonateSocketPeer</b> should be called after the <a href="/windows/desktop/api/winsock2/nf-winsock2-accept">accept</a>, <a href="/windows/desktop/api/mswsock/nf-mswsock-acceptex">AcceptEx</a>, or <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaccept">WSAAccept</a> function returns.  

For connectionless sockets, the application should call the <b>WSAImpersonateSocketPeer</b> function immediately after the <a href="/windows/desktop/api/winsock/nf-winsock-recv">recv</a>, <a href="/windows/desktop/api/winsock/nf-winsock-recvfrom">recvfrom</a>, <a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecv">WSARecv</a>, <a href="/windows/desktop/api/mswsock/nf-mswsock-wsarecvex">WSARecvEx</a>, <a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecvfrom">WSARecvFrom</a>, or <a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg">LPFN_WSARECVMSG (WSARecvMsg)</a> function returns for a new peer address. 

The <b>WSAImpersonateSocketPeer</b> function can be called multiple times for a single socket.  

An error will be returned if the following conditions are not met.<ul>
<li>The address family of the <i>Socket</i> parameter must be either AF_INET or AF_INET6.</li>
<li>The socket type must be either SOCK_STREAM or SOCK_DGRAM.</li>
</ul>


The <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsarevertimpersonation">WSARevertImpersonation</a> function must be called to end the impersonation.

## -see-also

<a href="/windows/desktop/api/mswsock/nf-mswsock-acceptex">AcceptEx</a>



<a href="/windows/desktop/WinSock/using-secure-socket-extensions">Using Secure Socket Extensions</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaccept">WSAAccept</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname">WSADeleteSocketPeerTargetName</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity">WSAQuerySocketSecurity</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecv">WSARecv</a>



<a href="/windows/desktop/api/mswsock/nf-mswsock-wsarecvex">WSARecvEx</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecvfrom">WSARecvFrom</a>



<a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg">LPFN_WSARECVMSG (WSARecvMsg)</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsarevertimpersonation">WSARevertImpersonation</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname">WSASetSocketPeerTargetName</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity">WSASetSocketSecurity</a>



<a href="/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Filtering Platform</a>



<a href="/windows/desktop/FWP/fwp-functions">Windows Filtering Platform  API  Functions</a>



<a href="/windows/desktop/WinSock/winsock-secure-socket-extensions">Winsock Secure Socket Extensions</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-accept">accept</a>



<a href="/windows/desktop/api/winsock/nf-winsock-recv">recv</a>



<a href="/windows/desktop/api/winsock/nf-winsock-recvfrom">recvfrom</a>