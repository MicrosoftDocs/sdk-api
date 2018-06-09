---
UID: NF:ws2tcpip.WSAImpersonateSocketPeer
title: WSAImpersonateSocketPeer function
author: windows-sdk-content
description: Used to impersonate the security principal corresponding to a socket peer in order to perform application-level authorization.
old-location: winsock\wsaimpersonatesocketpeer.htm
old-project: WinSock
ms.assetid: 8dd2c0dd-ca1d-40b8-8e58-a980e67b6941
ms.author: windowssdkdev
ms.date: 04/30/2018
ms.keywords: WSAImpersonateSocketPeer, WSAImpersonateSocketPeer function [Winsock], winsock.wsaimpersonatesocketpeer, ws2tcpip/WSAImpersonateSocketPeer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: WSPUPCALLTABLE, *LPWSPUPCALLTABLE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Fwpuclnt.dll
api_name:
 - WSAImpersonateSocketPeer
product: Windows
targetos: Windows
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSAImpersonateSocketPeer function


## -description


The <b>WSAImpersonateSocketPeer</b> function is used to impersonate the security principal corresponding to a socket peer in order to perform application-level authorization.


## -parameters




### -param Socket [in]

Identifies the application socket.


### -param PeerAddr

TBD


### -param PeerAddrLen

TBD




#### - PeerAddress [in, optional]

The IP address of the peer to be impersonated.  For connection-oriented sockets, the connected socket uniquely identifies a peer.  In this case, this parameter is ignored.


#### - peerAddressLen [in]

The size, in bytes, of the <i>PeerAddress</i> parameter.


## -returns



If the function succeeds, the return value is 0.  Otherwise, a value of <b>SOCKET_ERROR</b> is returned, and a specific error code can be retrieved by calling 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>. 

Some possible error codes are listed below.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop//WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The system detected an invalid address pointer in attempting to use a pointer argument of a call. This error is returned if the <i>PeerAddr</i> parameter was a <b>NULL</b> pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop//WinSock/windows-sockets-error-codes-2">WSAEAFNOSUPPORT</a></b></dt>
</dl>
</td>
<td width="60%">
The specified address family is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop//WinSock/windows-sockets-error-codes-2">WSAEMSGSIZE</a></b></dt>
</dl>
</td>
<td width="60%">
A buffer passed was too small. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop//WinSock/windows-sockets-error-codes-2">WSAENOTSOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The descriptor passed in the <i>Socket</i> parameter is not a valid socket.

</td>
</tr>
</table>
 




## -remarks



The <b>WSAImpersonateSocketPeer</b> function provides an application the ability to impersonate the security principal corresponding to a socket peer in order to perform application-level authorization. If peer user (impersonation) token is available then it will be used for impersonation, otherwise the peer computer token will be used. The <b>WSAImpersonateSocketPeer</b> function can be called only for blocking, non-overlapped sockets. After performing any authorization checks, an application must call the <a href="https://msdn.microsoft.com/7de25015-97ec-4338-846f-57df54142d65">WSARevertImpersonation</a> function to terminate the impersonation.

For connection-oriented sockets, the <b>WSAImpersonateSocketPeer</b> function should be called after a connection is established. For a server application using connection-oriented sockets, the <b>WSAImpersonateSocketPeer</b> should be called after the <a href="https://msdn.microsoft.com/72246263-4806-4ab2-9b26-89a1782a954b">accept</a>, <a href="https://msdn.microsoft.com/cfd4c169-a8af-46cc-9b0e-fd7fb5aad61b">AcceptEx</a>, or <a href="https://msdn.microsoft.com/f385f63f-49b2-4eb7-8717-ad4cca1a2252">WSAAccept</a> function returns.  

For connectionless sockets, the application should call the <b>WSAImpersonateSocketPeer</b> function immediately after the <a href="https://msdn.microsoft.com/8c247cd3-479f-45d0-a038-a24e80cc7c73">recv</a>, <a href="https://msdn.microsoft.com/3e4282e0-3ed0-43e7-9b27-72ec36b9cfa1">recvfrom</a>, <a href="https://msdn.microsoft.com/bfe66e11-e9a7-4321-ad55-3141113e9a03">WSARecv</a>, <a href="https://msdn.microsoft.com/0ed639f7-e7bd-49a2-a7c0-177699a2cf5e">WSARecvEx</a>, <a href="https://msdn.microsoft.com/8617dbb8-0e4e-4cd3-9597-5d20de6778f6">WSARecvFrom</a>, or <a href="https://msdn.microsoft.com/a46449f7-3206-45e9-9df0-f272b8cdcc4b">WSARecvMsg</a> function returns for a new peer address. 

The <b>WSAImpersonateSocketPeer</b> function can be called multiple times for a single socket.  

An error will be returned if the following conditions are not met.<ul>
<li>The address family of the <i>Socket</i> parameter must be either AF_INET or AF_INET6.</li>
<li>The socket type must be either SOCK_STREAM or SOCK_DGRAM.</li>
</ul>


The <a href="https://msdn.microsoft.com/7de25015-97ec-4338-846f-57df54142d65">WSARevertImpersonation</a> function must be called to end the impersonation.




## -see-also




<a href="https://msdn.microsoft.com/cfd4c169-a8af-46cc-9b0e-fd7fb5aad61b">AcceptEx</a>



<a href="https://msdn.microsoft.com/d5e2f9d0-c61f-42d3-b62b-6c75b221ae24">Using Secure Socket Extensions</a>



<a href="https://msdn.microsoft.com/f385f63f-49b2-4eb7-8717-ad4cca1a2252">WSAAccept</a>



<a href="https://msdn.microsoft.com/5d973316-fc51-453e-8d98-36ba36367df7">WSADeleteSocketPeerTargetName</a>



<a href="https://msdn.microsoft.com/fda7738f-b7fc-49c3-aa40-9beea31d1009">WSAQuerySocketSecurity</a>



<a href="https://msdn.microsoft.com/bfe66e11-e9a7-4321-ad55-3141113e9a03">WSARecv</a>



<a href="https://msdn.microsoft.com/0ed639f7-e7bd-49a2-a7c0-177699a2cf5e">WSARecvEx</a>



<a href="https://msdn.microsoft.com/8617dbb8-0e4e-4cd3-9597-5d20de6778f6">WSARecvFrom</a>



<a href="https://msdn.microsoft.com/a46449f7-3206-45e9-9df0-f272b8cdcc4b">WSARecvMsg</a>



<a href="https://msdn.microsoft.com/7de25015-97ec-4338-846f-57df54142d65">WSARevertImpersonation</a>



<a href="https://msdn.microsoft.com/c293658c-d7f9-411d-b6c1-a333592a741c">WSASetSocketPeerTargetName</a>



<a href="https://msdn.microsoft.com/9efee804-9763-4456-97a3-6eb9a8e30f49">WSASetSocketSecurity</a>



<a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Filtering Platform</a>



<a href="https://msdn.microsoft.com/26a69710-9981-40a4-8b1e-dca709624ead">Windows Filtering Platform  API  Functions</a>



<a href="https://msdn.microsoft.com/023a9f96-814f-40c3-a186-ae0a0c9baef2">Winsock Secure Socket Extensions</a>



<a href="https://msdn.microsoft.com/72246263-4806-4ab2-9b26-89a1782a954b">accept</a>



<a href="https://msdn.microsoft.com/8c247cd3-479f-45d0-a038-a24e80cc7c73">recv</a>



<a href="https://msdn.microsoft.com/3e4282e0-3ed0-43e7-9b27-72ec36b9cfa1">recvfrom</a>
 

 

