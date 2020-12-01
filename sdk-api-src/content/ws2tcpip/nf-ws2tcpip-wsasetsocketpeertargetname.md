---
UID: NF:ws2tcpip.WSASetSocketPeerTargetName
title: WSASetSocketPeerTargetName function (ws2tcpip.h)
description: Is used to specify the peer target name (SPN) that corresponds to a peer IP address. This target name is meant to be specified by client applications to securely identify the peer that should be authenticated.
helpviewer_keywords: ["WSASetSocketPeerTargetName","WSASetSocketPeerTargetName function [Winsock]","winsock.wsasetsocketpeertargetname","ws2tcpip/WSASetSocketPeerTargetName"]
old-location: winsock\wsasetsocketpeertargetname.htm
tech.root: WinSock
ms.assetid: c293658c-d7f9-411d-b6c1-a333592a741c
ms.date: 12/05/2018
ms.keywords: WSASetSocketPeerTargetName, WSASetSocketPeerTargetName function [Winsock], winsock.wsasetsocketpeertargetname, ws2tcpip/WSASetSocketPeerTargetName
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
 - WSASetSocketPeerTargetName
 - ws2tcpip/WSASetSocketPeerTargetName
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
 - WSASetSocketPeerTargetName
---

# WSASetSocketPeerTargetName function


## -description

The <b>WSASetSocketPeerTargetName</b> function is used to specify the peer target name (SPN) that corresponds to a peer IP address.  This target name is meant to be specified by client applications to securely identify the peer that should be authenticated.

## -parameters

### -param Socket [in]

A descriptor identifying a socket on which the peer target name is being assigned.

### -param PeerTargetName [in]

A pointer to a <a href="/windows/desktop/api/mstcpip/ns-mstcpip-socket_peer_target_name">SOCKET_PEER_TARGET_NAME</a> structure that defines the peer target name.

### -param PeerTargetNameLen [in]

The size, in bytes, of the <i>PeerTargetName</i> parameter.

### -param Overlapped [in, optional]

A pointer to a <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped">WSAOVERLAPPED</a> structure.  This parameter is ignored for non-overlapped sockets.

### -param CompletionRoutine [in, optional]

A pointer to the completion routine called when the operation has been completed.  This parameter is ignored for non-overlapped sockets.

## -returns

If the function succeeds, the return value is zero.  Otherwise, a value of <b>SOCKET_ERROR</b> is returned, and a specific error code can be retrieved by calling 
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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The system detected an invalid address pointer in attempting to use a pointer argument of a call. This error is returned if the <i>PeerTargetName</i> parameter was a <b>NULL</b> pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed. This error is returned if the socket passed in the <i>Socket</i> parameter was not created with an address family of the <b>AF_INET</b> or <b>AF_INET6</b> and a socket type of <b>SOCK_DGRAM</b> or <b>SOCK_STREAM</b>.  This error is also returned for a connectionless socket if the IP address and port are zero in the <b>PeerAddress</b> member of the <a href="/windows/desktop/api/mstcpip/ns-mstcpip-socket_peer_target_name">SOCKET_PEER_TARGET_NAME</a> structure pointed to by the <i>PeerTargetName</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEISCONN</a></b></dt>
</dl>
</td>
<td width="60%">
The socket is connected. This function is not permitted with a connected socket, whether the socket is connection oriented or connectionless.

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

The <b>WSASetSocketPeerTargetName</b> function provides a method to specify the target name that corresponds to a peer security principal. This function is meant to be used by a client application to identify the peer that should be authenticated. A client application should specify the peer target name in order to prevent trusted man-in-the-middle attacks. For connectionless sockets, an application can call the <b>WSASetSocketPeerTargetName</b> function multiple times to specify different target names for different peer IP addresses.

This function simplifies having to call the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a> function with a <i>dwIoControlCode</i> parameter set to <b>SIO_SET_PEER_TARGET_NAME</b>. 

For connection-oriented sockets, the <b>WSASetSocketPeerTargetName</b> function should be called before <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnect">WSAConnect</a>.  For connectionless sockets, this function should be called before <b>WSAConnect</b> or before the first <a href="/windows/desktop/api/winsock2/nf-winsock2-wsasendto">WSASendTo</a> call directed to the peer address.

An error will be returned if the following conditions are not met.<ul>
<li>The address family of the <i>Socket</i> parameter must be either AF_INET or AF_INET6.</li>
<li>The socket type must be either SOCK_STREAM or SOCK_DGRAM.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mstcpip/ns-mstcpip-socket_peer_target_name">SOCKET_PEER_TARGET_NAME</a>



<a href="/windows/desktop/WinSock/using-secure-socket-extensions">Using Secure Socket Extensions</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname">WSADeleteSocketPeerTargetName</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer">WSAImpersonateSocketPeer</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity">WSAQuerySocketSecurity</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsarevertimpersonation">WSARevertImpersonation</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity">WSASetSocketSecurity</a>



<a href="/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Filtering Platform</a>



<a href="/windows/desktop/FWP/fwp-functions">Windows Filtering Platform  API  Functions</a>



<a href="/windows/desktop/WinSock/winsock-secure-socket-extensions">Winsock Secure Socket Extensions</a>