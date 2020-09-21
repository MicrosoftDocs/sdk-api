---
UID: NF:ws2tcpip.WSADeleteSocketPeerTargetName
title: WSADeleteSocketPeerTargetName function (ws2tcpip.h)
description: Removes the association between a peer target name and an IP address for a socket. After a successful return, there will be no future association between the IP address and the target name.
helpviewer_keywords: ["WSADeleteSocketPeerTargetName","WSADeleteSocketPeerTargetName function [Winsock]","winsock.wsadeletesocketpeertargetname","ws2tcpip/WSADeleteSocketPeerTargetName"]
old-location: winsock\wsadeletesocketpeertargetname.htm
tech.root: WinSock
ms.assetid: 5d973316-fc51-453e-8d98-36ba36367df7
ms.date: 12/05/2018
ms.keywords: WSADeleteSocketPeerTargetName, WSADeleteSocketPeerTargetName function [Winsock], winsock.wsadeletesocketpeertargetname, ws2tcpip/WSADeleteSocketPeerTargetName
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
 - WSADeleteSocketPeerTargetName
 - ws2tcpip/WSADeleteSocketPeerTargetName
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
 - WSADeleteSocketPeerTargetName
---

# WSADeleteSocketPeerTargetName function


## -description

The <b>WSADeleteSocketPeerTargetName</b> function removes the association between a peer target name and an IP address for a socket.  After a successful return, there will be no future association between the IP address and the target name.

## -parameters

### -param Socket [in]

A descriptor identifying a socket on which the peer target name is being deleted.

### -param PeerAddr [in]

The IP address of the peer for which the target name is being deleted.

### -param PeerAddrLen [in]

The size, in bytes, of the <i>PeerAddr</i> parameter.

### -param Overlapped [in, optional]

A pointer to a <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped">WSAOVERLAPPED</a> structure.  This parameter is ignored for non-overlapped sockets.

### -param CompletionRoutine [in, optional]

A pointer to the completion routine called when the operation has been completed.  This parameter is ignored for non-overlapped sockets.

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
The system detected an invalid address pointer in attempting to use a pointer argument of a call. This error is returned if the <i>PeerAddr</i> parameter was a <b>NULL</b> pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed. This error is returned if the socket passed in the <i>Socket</i> parameter was not created with an address family of the <b>AF_INET</b> or <b>AF_INET6</b> and a socket type of <b>SOCK_DGRAM</b> or <b>SOCK_STREAM</b>.  

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

The <b>WSADeleteSocketPeerTargetName</b> function provides a method to remove the association between a peer target name and an IP address for a socket. This function is used to delete a peer target name that was previously set with the <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname">WSASetSocketPeerTargetName</a> function.  After the <b>WSADeleteSocketPeerTargetName</b> function returns, no future authentication to the IP address will use the previously specified target name. This function is primarily designed to be used by connectionless clients (for example, a socket created with the type set to SOCK_DGRAM or the protocol set to IPPROTO_UDP) after they have terminated the connection with the IP	address associated with the peer target name. For connection oriented clients (for example, a socket created with the type set to SOCK_STREAM or protocol set to IPPROTO_TCP), this function should not be called.

The <b>WSADeleteSocketPeerTargetName</b> function  simplifies having to call the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a> function with a <i>dwIoControlCode</i> parameter set to <b>SIO_DELETE_PEER_TARGET_NAME</b>. 

An error will be returned if the following conditions are not met.<ul>
<li>The address family of the <i>Socket</i> parameter must be either AF_INET or AF_INET6.</li>
<li>The socket type must be either SOCK_STREAM or SOCK_DGRAM.</li>
</ul>

## -see-also

<a href="/windows/desktop/WinSock/using-secure-socket-extensions">Using Secure Socket Extensions</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer">WSAImpersonateSocketPeer</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity">WSAQuerySocketSecurity</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsarevertimpersonation">WSARevertImpersonation</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname">WSASetSocketPeerTargetName</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity">WSASetSocketSecurity</a>



<a href="/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Filtering Platform</a>



<a href="/windows/desktop/FWP/fwp-functions">Windows Filtering Platform  API  Functions</a>



<a href="/windows/desktop/WinSock/winsock-secure-socket-extensions">Winsock Secure Socket Extensions</a>