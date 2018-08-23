---
UID: NS:mstcpip._SOCKET_PEER_TARGET_NAME
title: "_SOCKET_PEER_TARGET_NAME"
author: windows-sdk-content
description: Contains the IP address and name for a peer target and the type of security protocol to be used on a socket.
old-location: winsock\socket_peer_target_name.htm
old-project: winsock
ms.assetid: 6e807cc3-f9de-4d15-b337-4a6b4be910c2
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: SOCKET_PEER_TARGET_NAME, SOCKET_PEER_TARGET_NAME structure [Winsock], _SOCKET_PEER_TARGET_NAME, mstcpip/SOCKET_PEER_TARGET_NAME, winsock.socket_peer_target_name
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mstcpip.h
req.include-header: 
req.redist: 
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
req.typenames: SOCKET_PEER_TARGET_NAME
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mstcpip.h
api_name:
 - SOCKET_PEER_TARGET_NAME
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _SOCKET_PEER_TARGET_NAME structure


## -description


The <b>SOCKET_PEER_TARGET_NAME</b> structure contains the IP address and name for a peer target and the type of security protocol to be used on a socket.


## -struct-fields




### -field SecurityProtocol

A <a href="https://msdn.microsoft.com/ae77ac61-5035-401e-a4b6-345c1be7b2b7">SOCKET_SECURITY_PROTOCOL</a> value that identifies the type of protocol used to secure the traffic on the socket.


### -field PeerAddress

The IP address of the peer for the socket.


### -field PeerTargetNameStringLen

The length, in bytes, of the peer target name in the <b>AllStrings</b> member.


### -field AllStrings

The peer target name for the socket.


## -remarks



The <b>SOCKET_PEER_TARGET_NAME</b> structure  is supported on Windows Vistaand later.

The <b>SOCKET_PEER_TARGET_NAME</b> structure  is used by the <a href="https://msdn.microsoft.com/c293658c-d7f9-411d-b6c1-a333592a741c">WSASetSocketPeerTargetName</a> function to specify the peer target name that corresponds to a peer IP address.  This target name is meant to be specified by client applications to securely identify the peer that should be authenticated.

Currently, the only type of security protocol that is supported is IPsec. So specifying an enumeration value  of <b>SOCKET_SECURITY_PROTOCOL_DEFAULT</b> has the same effect as specifying <b>SOCKET_SECURITY_PROTOCOL_IPSEC</b> in the <b>SecurityProtocol</b> member. 

The implementation of IPsec on Windows Vistaand Windows Server 2008 only supports computer-to-computer and user-to-computer authentication. As a result, the peer target name specified in the <b>AllStrings</b> member of the <b>SOCKET_PEER_TARGET_NAME</b> structure  should refer to the peer computer principal.




## -see-also




<a href="https://msdn.microsoft.com/dfd84b91-0a94-4fe6-b8d2-18562afb9c24">SOCKADDR_STORAGE</a>



<a href="https://msdn.microsoft.com/ae77ac61-5035-401e-a4b6-345c1be7b2b7">SOCKET_SECURITY_PROTOCOL</a>



<a href="https://msdn.microsoft.com/d5e2f9d0-c61f-42d3-b62b-6c75b221ae24">Using Secure Socket Extensions</a>



<a href="https://msdn.microsoft.com/c293658c-d7f9-411d-b6c1-a333592a741c">WSASetSocketPeerTargetName</a>



<a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Filtering Platform</a>



<a href="https://msdn.microsoft.com/26a69710-9981-40a4-8b1e-dca709624ead">Windows Filtering Platform  API  Functions</a>



<a href="https://msdn.microsoft.com/023a9f96-814f-40c3-a186-ae0a0c9baef2">Winsock Secure Socket Extensions</a>
 

 

