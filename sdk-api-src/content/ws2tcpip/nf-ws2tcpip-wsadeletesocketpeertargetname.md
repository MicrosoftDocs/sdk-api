---
UID: NF:ws2tcpip.WSADeleteSocketPeerTargetName
title: WSADeleteSocketPeerTargetName function
author: windows-sdk-content
description: Removes the association between a peer target name and an IP address for a socket. After a successful return, there will be no future association between the IP address and the target name.
old-location: winsock\wsadeletesocketpeertargetname.htm
tech.root: winsock
ms.assetid: 5d973316-fc51-453e-8d98-36ba36367df7
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: WSADeleteSocketPeerTargetName, WSADeleteSocketPeerTargetName function [Winsock], winsock.wsadeletesocketpeertargetname, ws2tcpip/WSADeleteSocketPeerTargetName
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
 - WSADeleteSocketPeerTargetName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- WSADeleteSocketPeerTargetName
: 
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

A pointer to a <a href="https://msdn.microsoft.com/91004241-e0ea-4bda-a0f5-71688ac83038">WSAOVERLAPPED</a> structure.  This parameter is ignored for non-overlapped sockets.


### -param CompletionRoutine [in, optional]

A pointer to the completion routine called when the operation has been completed.  This parameter is ignored for non-overlapped sockets.


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
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEAFNOSUPPORT</a></b></dt>
</dl>
</td>
<td width="60%">
The specified address family is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The system detected an invalid address pointer in attempting to use a pointer argument of a call. This error is returned if the <i>PeerAddr</i> parameter was a <b>NULL</b> pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed. This error is returned if the socket passed in the <i>Socket</i> parameter was not created with an address family of the <b>AF_INET</b> or <b>AF_INET6</b> and a socket type of <b>SOCK_DGRAM</b> or <b>SOCK_STREAM</b>.  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEMSGSIZE</a></b></dt>
</dl>
</td>
<td width="60%">
A buffer passed was too small. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAENOTSOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The descriptor passed in the <i>Socket</i> parameter is not a valid socket.

</td>
</tr>
</table>
 




## -remarks



The <b>WSADeleteSocketPeerTargetName</b> function provides a method to remove the association between a peer target name and an IP address for a socket. This function is used to delete a peer target name that was previously set with the <a href="https://msdn.microsoft.com/c293658c-d7f9-411d-b6c1-a333592a741c">WSASetSocketPeerTargetName</a> function.  After the <b>WSADeleteSocketPeerTargetName</b> function returns, no future authentication to the IP address will use the previously specified target name. This function is primarily designed to be used by connectionless clients (for example, a socket created with the type set to SOCK_DGRAM or the protocol set to IPPROTO_UDP) after they have terminated the connection with the IP	address associated with the peer target name. For connection oriented clients (for example, a socket created with the type set to SOCK_STREAM or protocol set to IPPROTO_TCP), this function should not be called.

The <b>WSADeleteSocketPeerTargetName</b> function  simplifies having to call the <a href="https://msdn.microsoft.com/038aeca6-d7b7-4f74-ac69-4536c2e5118b">WSAIoctl</a> function with a <i>dwIoControlCode</i> parameter set to <b>SIO_DELETE_PEER_TARGET_NAME</b>. 

An error will be returned if the following conditions are not met.<ul>
<li>The address family of the <i>Socket</i> parameter must be either AF_INET or AF_INET6.</li>
<li>The socket type must be either SOCK_STREAM or SOCK_DGRAM.</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/d5e2f9d0-c61f-42d3-b62b-6c75b221ae24">Using Secure Socket Extensions</a>



<a href="https://msdn.microsoft.com/8dd2c0dd-ca1d-40b8-8e58-a980e67b6941">WSAImpersonateSocketPeer</a>



<a href="https://msdn.microsoft.com/fda7738f-b7fc-49c3-aa40-9beea31d1009">WSAQuerySocketSecurity</a>



<a href="https://msdn.microsoft.com/7de25015-97ec-4338-846f-57df54142d65">WSARevertImpersonation</a>



<a href="https://msdn.microsoft.com/c293658c-d7f9-411d-b6c1-a333592a741c">WSASetSocketPeerTargetName</a>



<a href="https://msdn.microsoft.com/9efee804-9763-4456-97a3-6eb9a8e30f49">WSASetSocketSecurity</a>



<a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Filtering Platform</a>



<a href="https://msdn.microsoft.com/26a69710-9981-40a4-8b1e-dca709624ead">Windows Filtering Platform  API  Functions</a>



<a href="https://msdn.microsoft.com/023a9f96-814f-40c3-a186-ae0a0c9baef2">Winsock Secure Socket Extensions</a>
 

 

