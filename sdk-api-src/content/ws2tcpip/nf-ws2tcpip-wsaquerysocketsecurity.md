---
UID: NF:ws2tcpip.WSAQuerySocketSecurity
title: WSAQuerySocketSecurity function
author: windows-sdk-content
description: Queries information about the security applied to a connection on a socket.
old-location: winsock\wsaquerysocketsecurity.htm
tech.root: winsock
ms.assetid: fda7738f-b7fc-49c3-aa40-9beea31d1009
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WSAQuerySocketSecurity, WSAQuerySocketSecurity function [Winsock], winsock.wsaquerysocketsecurity, ws2tcpip/WSAQuerySocketSecurity
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Fwpuclnt.dll
api_name:
 - WSAQuerySocketSecurity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WSAQuerySocketSecurity function


## -description


The <b>WSAQuerySocketSecurity</b> function queries information about the security applied to a connection on a socket.


## -parameters




### -param Socket [in]

A descriptor identifying a socket for which security information is being queried.


### -param SecurityQueryTemplate [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/cd222287-c4f2-4c4b-8b5f-81b6fcbe87d4">SOCKET_SECURITY_QUERY_TEMPLATE</a> structure that specifies the type of query information to return. 

A <a href="https://msdn.microsoft.com/cd222287-c4f2-4c4b-8b5f-81b6fcbe87d4">SOCKET_SECURITY_QUERY_TEMPLATE</a> structure pointed to by this parameter may contain zeroes for all members to request default security information. On successful return, only the <b>Flags</b> member in the <a href="https://msdn.microsoft.com/90439ff6-e6a8-4124-b280-a65b9ca12787">SOCKET_SECURITY_QUERY_INFO</a> will be set in the returned  <i>SecurityQueryInfo</i> parameter. 

This parameter may be a <b>NULL</b> pointer if the <i>Socket</i> parameter was created with a protocol of <b>IPPROTO_TCP</b>. In this case, the information returned is the same as if a <a href="https://msdn.microsoft.com/cd222287-c4f2-4c4b-8b5f-81b6fcbe87d4">SOCKET_SECURITY_QUERY_TEMPLATE</a> structure with all values set to zero was passed. This parameter should be specified for a socket with protocol of <b>IPPROTO_TCP</b> if more than the default security information is required. 

If the <a href="https://msdn.microsoft.com/cd222287-c4f2-4c4b-8b5f-81b6fcbe87d4">SOCKET_SECURITY_QUERY_TEMPLATE</a> structure  is specified with the <b>PeerTokenAccessMask</b> member not specified (set to zero), then the <b>WSAQuerySocketSecurity</b> function will not return the <b>PeerApplicationAccessTokenHandle</b> and <b>PeerMachineAccessTokenHandle</b> members in the <a href="https://msdn.microsoft.com/90439ff6-e6a8-4124-b280-a65b9ca12787">SOCKET_SECURITY_QUERY_INFO</a> structure.

If a <i>Socket</i> parameter was created with a protocol not equal to <b>IPPROTO_TCP</b>, the <i>SecurityQueryTemplate</i> parameter must be specified. In these cases, the <b>PeerAddress</b> member of the <a href="https://msdn.microsoft.com/cd222287-c4f2-4c4b-8b5f-81b6fcbe87d4">SOCKET_SECURITY_QUERY_TEMPLATE</a> structure must specify an address family of AF_INET or AF_INET6 along with peer IP address and port number.


### -param SecurityQueryTemplateLen [in]

The size, in bytes, of the <i>SecurityQueryTemplate</i> parameter. 

This parameter may be a zero if the <i>Socket</i> parameter was created with a protocol of <b>IPPROTO_TCP</b>. Otherwise, this parameter must be the size of a <a href="https://msdn.microsoft.com/cd222287-c4f2-4c4b-8b5f-81b6fcbe87d4">SOCKET_SECURITY_QUERY_TEMPLATE</a> structure. 


### -param SecurityQueryInfo [out, optional]

A pointer to a buffer that will receive a <a href="https://msdn.microsoft.com/90439ff6-e6a8-4124-b280-a65b9ca12787">SOCKET_SECURITY_QUERY_INFO</a> structure containing the information queried.  This value can be set to <b>NULL</b> to query the size of the output buffer.


### -param SecurityQueryInfoLen [in, out]

On input, a pointer to the size, in bytes, of the <i>SecurityQueryInfo</i> parameter.   If the buffer is too small to receive the queried information, the call will return SOCKET_ERROR, and the number of bytes needed to return the queried information will be set in the value pointed to by this parameter.  On a successful call, the number of bytes copied is returned.


### -param Overlapped [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/91004241-e0ea-4bda-a0f5-71688ac83038">WSAOVERLAPPED</a> structure.  This parameter is ignored for non-overlapped sockets.


### -param CompletionRoutine [in, optional]

A pointer to the completion routine called when the operation has been completed.  This parameter is ignored for non-overlapped sockets.


## -returns



If the function succeeds, the return value is zero.  Otherwise, a value of <b>SOCKET_ERROR</b> is returned, and a specific error code can be retrieved by calling 
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
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEAFNOSUPPORT</a></b></dt>
</dl>
</td>
<td width="60%">
The specified address family is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAECONNRESET</a></b></dt>
</dl>
</td>
<td width="60%">
For a stream socket, the virtual circuit was reset by the remote side. The application should close the socket as it is no longer usable. For a UDP datagram socket, this error would indicate that a previous send operation resulted in an ICMP "Port Unreachable" message.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The system detected an invalid pointer address in attempting to use a parameter. This error is returned if the <i>SecurityQueryInfoLen</i> parameter was a <b>NULL</b> pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed. This error is returned if the socket passed in the <i>Socket</i> parameter was not created with an address family of the <b>AF_INET</b> or <b>AF_INET6</b> and a socket type of <b>SOCK_DGRAM</b> or <b>SOCK_STREAM</b>.  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEMSGSIZE</a></b></dt>
</dl>
</td>
<td width="60%">
A buffer passed was too small. This error is returned for a <i>Socket</i> parameter when the protocol was not <b>IPPROTO_TCP</b> if the  <i>SecurityQueryInfo</i> parameter is a <b>NULL</b> pointer or the  <i>SecurityQueryTemplateLen</i> parameter is less than the size of a <a href="https://msdn.microsoft.com/cd222287-c4f2-4c4b-8b5f-81b6fcbe87d4">SOCKET_SECURITY_QUERY_TEMPLATE</a> structure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAENOTSOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The descriptor passed in the <i>Socket</i> parameter is not a valid socket.

</td>
</tr>
</table>
 




## -remarks



The <b>WSAQuerySocketSecurity</b> function provides a method to query the current security settings on a socket. After a connection is established, the <b>WSAQuerySocketSecurity</b> function allows an application to query the security properties of the connection, which can include information on peer access tokens.

For connection-oriented sockets, it is preferred to call the <b>WSAQuerySocketSecurity</b> function immediately after a connection is established. For connectionless sockets, it is preferred to call the <b>WSAQuerySocketSecurity</b> function immediately after data is sent to a new peer address or received from a new peer address. The <b>WSAQuerySocketSecurity</b> function can be called multiple times on a single socket.

This function simplifies having to call the <a href="https://msdn.microsoft.com/038aeca6-d7b7-4f74-ac69-4536c2e5118b">WSAIoctl</a> function with a <i>dwIoControlCode</i> parameter set to <b>SIO_QUERY_SECURITY</b>.

The <b>WSAQuerySocketSecurity</b> function may be called on a <i>Socket</i> parameter created with an address family of <b>AF_INET</b> or <b>AF_INET6</b>.

If the <i>Socket</i> parameter was created with a protocol of <b>IPPROTO_TCP</b>, the <i>SecurityQueryTemplate</i> parameter may be <b>NULL</b> and the <i>SecurityQueryTemplateLen</i> parameter may be zero. Otherwise, the <i>SecurityQueryTemplate</i> parameter must point to a <a href="https://msdn.microsoft.com/cd222287-c4f2-4c4b-8b5f-81b6fcbe87d4">SOCKET_SECURITY_QUERY_TEMPLATE</a> structure.

For a client application using connection-oriented sockets (socket created with a protocol of <b>IPPROTO_TCP</b>), the <b>WSAQuerySocketSecurity</b> function should be called after the <a href="https://msdn.microsoft.com/13468139-dc03-45bd-850c-7ac2dbcb6e60">connect</a>, <a href="https://msdn.microsoft.com/a4552366-eafa-4f24-b6c2-e6a7edc4b021">ConnectEx</a>, or <a href="https://msdn.microsoft.com/3b32cc6e-3df7-4104-a0d4-317fd445c7b2">WSAConnect</a> function returns.  For a server application using connection-oriented sockets (protocol of <b>IPPROTO_TCP</b>), the <b>WSAQuerySocketSecurity</b> function should be called after the <a href="https://msdn.microsoft.com/72246263-4806-4ab2-9b26-89a1782a954b">accept</a>, <a href="https://msdn.microsoft.com/cfd4c169-a8af-46cc-9b0e-fd7fb5aad61b">AcceptEx</a>, or <a href="https://msdn.microsoft.com/f385f63f-49b2-4eb7-8717-ad4cca1a2252">WSAAccept</a> function returns.

For connectionless sockets (socket created with a protocol of <b>IPPROTO_UDP</b>), the application should call the <b>WSAQuerySocketSecurity</b> function immediately after <a href="https://msdn.microsoft.com/e3a11522-871c-4d6b-a2e6-ca91ffc2b698">WSASendTo</a> or <a href="https://msdn.microsoft.com/8617dbb8-0e4e-4cd3-9597-5d20de6778f6">WSARecvFrom</a> call returns for a new peer address.

An error will be returned if the following conditions are not met.<ul>
<li>The address family of the <i>Socket</i> parameter must be either AF_INET or AF_INET6.</li>
<li>The socket type must be either SOCK_STREAM or SOCK_DGRAM.</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/90439ff6-e6a8-4124-b280-a65b9ca12787">SOCKET_SECURITY_QUERY_INFO</a>



<a href="https://msdn.microsoft.com/cd222287-c4f2-4c4b-8b5f-81b6fcbe87d4">SOCKET_SECURITY_QUERY_TEMPLATE</a>



<a href="https://msdn.microsoft.com/d5e2f9d0-c61f-42d3-b62b-6c75b221ae24">Using Secure Socket Extensions</a>



<a href="https://msdn.microsoft.com/5d973316-fc51-453e-8d98-36ba36367df7">WSADeleteSocketPeerTargetName</a>



<a href="https://msdn.microsoft.com/8dd2c0dd-ca1d-40b8-8e58-a980e67b6941">WSAImpersonateSocketPeer</a>



<a href="https://msdn.microsoft.com/7de25015-97ec-4338-846f-57df54142d65">WSARevertImpersonation</a>



<a href="https://msdn.microsoft.com/c293658c-d7f9-411d-b6c1-a333592a741c">WSASetSocketPeerTargetName</a>



<a href="https://msdn.microsoft.com/9efee804-9763-4456-97a3-6eb9a8e30f49">WSASetSocketSecurity</a>



<a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Filtering Platform</a>



<a href="https://msdn.microsoft.com/26a69710-9981-40a4-8b1e-dca709624ead">Windows Filtering Platform  API  Functions</a>



<a href="https://msdn.microsoft.com/023a9f96-814f-40c3-a186-ae0a0c9baef2">Winsock Secure Socket Extensions</a>
 

 

