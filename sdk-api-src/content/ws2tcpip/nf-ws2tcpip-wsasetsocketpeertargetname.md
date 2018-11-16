---
UID: NF:ws2tcpip.WSASetSocketPeerTargetName
title: WSASetSocketPeerTargetName function
author: windows-sdk-content
description: Is used to specify the peer target name (SPN) that corresponds to a peer IP address. This target name is meant to be specified by client applications to securely identify the peer that should be authenticated.
old-location: winsock\wsasetsocketpeertargetname.htm
tech.root: WinSock
ms.assetid: c293658c-d7f9-411d-b6c1-a333592a741c
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: WSASetSocketPeerTargetName, WSASetSocketPeerTargetName function [Winsock], winsock.wsasetsocketpeertargetname, ws2tcpip/WSASetSocketPeerTargetName
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
 - WSASetSocketPeerTargetName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- WSASetSocketPeerTargetName
: 
---

# WSASetSocketPeerTargetName function


## -description


The <b>WSASetSocketPeerTargetName</b> function is used to specify the peer target name (SPN) that corresponds to a peer IP address.  This target name is meant to be specified by client applications to securely identify the peer that should be authenticated.


## -parameters




### -param Socket [in]

A descriptor identifying a socket on which the peer target name is being assigned. 


### -param PeerTargetName [in]

A pointer to a <a href="https://msdn.microsoft.com/6e807cc3-f9de-4d15-b337-4a6b4be910c2">SOCKET_PEER_TARGET_NAME</a> structure that defines the peer target name.


### -param PeerTargetNameLen [in]

The size, in bytes, of the <i>PeerTargetName</i> parameter.


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
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The system detected an invalid address pointer in attempting to use a pointer argument of a call. This error is returned if the <i>PeerTargetName</i> parameter was a <b>NULL</b> pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed. This error is returned if the socket passed in the <i>Socket</i> parameter was not created with an address family of the <b>AF_INET</b> or <b>AF_INET6</b> and a socket type of <b>SOCK_DGRAM</b> or <b>SOCK_STREAM</b>.  This error is also returned for a connectionless socket if the IP address and port are zero in the <b>PeerAddress</b> member of the <a href="https://msdn.microsoft.com/6e807cc3-f9de-4d15-b337-4a6b4be910c2">SOCKET_PEER_TARGET_NAME</a> structure pointed to by the <i>PeerTargetName</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEISCONN</a></b></dt>
</dl>
</td>
<td width="60%">
The socket is connected. This function is not permitted with a connected socket, whether the socket is connection oriented or connectionless.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEMSGSIZE</a></b></dt>
</dl>
</td>
<td width="60%">
A buffer passed was too small. 

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



The <b>WSASetSocketPeerTargetName</b> function provides a method to specify the target name that corresponds to a peer security principal. This function is meant to be used by a client application to identify the peer that should be authenticated. A client application should specify the peer target name in order to prevent trusted man-in-the-middle attacks. For connectionless sockets, an application can call the <b>WSASetSocketPeerTargetName</b> function multiple times to specify different target names for different peer IP addresses.

This function simplifies having to call the <a href="https://msdn.microsoft.com/038aeca6-d7b7-4f74-ac69-4536c2e5118b">WSAIoctl</a> function with a <i>dwIoControlCode</i> parameter set to <b>SIO_SET_PEER_TARGET_NAME</b>. 

For connection-oriented sockets, the <b>WSASetSocketPeerTargetName</b> function should be called before <a href="https://msdn.microsoft.com/3b32cc6e-3df7-4104-a0d4-317fd445c7b2">WSAConnect</a>.  For connectionless sockets, this function should be called before <b>WSAConnect</b> or before the first <a href="https://msdn.microsoft.com/e3a11522-871c-4d6b-a2e6-ca91ffc2b698">WSASendTo</a> call directed to the peer address.

An error will be returned if the following conditions are not met.<ul>
<li>The address family of the <i>Socket</i> parameter must be either AF_INET or AF_INET6.</li>
<li>The socket type must be either SOCK_STREAM or SOCK_DGRAM.</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/6e807cc3-f9de-4d15-b337-4a6b4be910c2">SOCKET_PEER_TARGET_NAME</a>



<a href="https://msdn.microsoft.com/d5e2f9d0-c61f-42d3-b62b-6c75b221ae24">Using Secure Socket Extensions</a>



<a href="https://msdn.microsoft.com/5d973316-fc51-453e-8d98-36ba36367df7">WSADeleteSocketPeerTargetName</a>



<a href="https://msdn.microsoft.com/8dd2c0dd-ca1d-40b8-8e58-a980e67b6941">WSAImpersonateSocketPeer</a>



<a href="https://msdn.microsoft.com/fda7738f-b7fc-49c3-aa40-9beea31d1009">WSAQuerySocketSecurity</a>



<a href="https://msdn.microsoft.com/7de25015-97ec-4338-846f-57df54142d65">WSARevertImpersonation</a>



<a href="https://msdn.microsoft.com/9efee804-9763-4456-97a3-6eb9a8e30f49">WSASetSocketSecurity</a>



<a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Filtering Platform</a>



<a href="https://msdn.microsoft.com/26a69710-9981-40a4-8b1e-dca709624ead">Windows Filtering Platform  API  Functions</a>



<a href="https://msdn.microsoft.com/023a9f96-814f-40c3-a186-ae0a0c9baef2">Winsock Secure Socket Extensions</a>
 

 

