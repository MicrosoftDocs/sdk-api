---
UID: NE:mstcpip._SOCKET_SECURITY_PROTOCOL
title: "_SOCKET_SECURITY_PROTOCOL"
author: windows-sdk-content
description: Indicates the type of security protocol to be used on a socket to secure network traffic.
old-location: winsock\socket_security_protocol.htm
tech.root: winsock
ms.assetid: ae77ac61-5035-401e-a4b6-345c1be7b2b7
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: SOCKET_SECURITY_PROTOCOL, SOCKET_SECURITY_PROTOCOL enumeration [Winsock], SOCKET_SECURITY_PROTOCOL_DEFAULT, SOCKET_SECURITY_PROTOCOL_INVALID, SOCKET_SECURITY_PROTOCOL_IPSEC, _SOCKET_SECURITY_PROTOCOL, mstcpip/SOCKET_SECURITY_PROTOCOL, mstcpip/SOCKET_SECURITY_PROTOCOL_DEFAULT, mstcpip/SOCKET_SECURITY_PROTOCOL_INVALID, mstcpip/SOCKET_SECURITY_PROTOCOL_IPSEC, winsock.socket_security_protocol
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: mstcpip.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mstcpip.h
api_name:
 - SOCKET_SECURITY_PROTOCOL
product: Windows
targetos: Windows
req.typenames: SOCKET_SECURITY_PROTOCOL
req.redist: 
---

# _SOCKET_SECURITY_PROTOCOL enumeration


## -description


The <b>SOCKET_SECURITY_PROTOCOL</b> enumeration indicates the type of security protocol to be used on a socket to secure network traffic.


## -enum-fields




### -field SOCKET_SECURITY_PROTOCOL_DEFAULT

The default system security will be used.


### -field SOCKET_SECURITY_PROTOCOL_IPSEC

IPsec will be used.


### -field SOCKET_SECURITY_PROTOCOL_IPSEC2


### -field SOCKET_SECURITY_PROTOCOL_INVALID

The maximum possible value for the <a href="https://msdn.microsoft.com/ae77ac61-5035-401e-a4b6-345c1be7b2b7">SOCKET_SECURITY_PROTOCOL</a> enumeration type. This is not a legal value.


## -remarks



This enumeration is supported on Windows Vistaand later.

Currently, the only type of security protocol that is supported is IPsec. So specifying an enumeration value  of <b>SOCKET_SECURITY_PROTOCOL_DEFAULT</b> has the same effect as specifying <b>SOCKET_SECURITY_PROTOCOL_IPSEC</b>. 

The <b>SOCKET_SECURITY_PROTOCOL</b> enumeration is used in the <a href="https://msdn.microsoft.com/6e807cc3-f9de-4d15-b337-4a6b4be910c2">SOCKET_PEER_TARGET_NAME</a>, <a href="https://msdn.microsoft.com/90439ff6-e6a8-4124-b280-a65b9ca12787">SOCKET_SECURITY_QUERY_INFO</a>, <a href="https://msdn.microsoft.com/cd222287-c4f2-4c4b-8b5f-81b6fcbe87d4">SOCKET_SECURITY_QUERY_TEMPLATE</a>, <a href="https://msdn.microsoft.com/9c47efb4-dd3e-4db9-a659-003292e2c5e9">SOCKET_SECURITY_SETTINGS</a>,  and <a href="https://msdn.microsoft.com/99af6ebd-6a7d-4753-8bc6-cfd42919843e">SOCKET_SECURITY_SETTINGS_IPSEC</a> structures to indicate the type of security protocol to be used on a socket in the <b>SecurityProtocol</b> member. These structures are used by the  <a href="https://msdn.microsoft.com/fda7738f-b7fc-49c3-aa40-9beea31d1009">WSAQuerySocketSecurity</a>, <a href="https://msdn.microsoft.com/c293658c-d7f9-411d-b6c1-a333592a741c">WSASetSocketPeerTargetName</a>, and <a href="https://msdn.microsoft.com/9efee804-9763-4456-97a3-6eb9a8e30f49">WSASetSocketSecurity</a> functions.

In addition to identifying the security protocol, this type is also used to decide how to interpret a pointer passed to some of the secure socket functions. This is analogous to how the <b>sa_family</b> member of the <a href="https://msdn.microsoft.com/d1392e1c-2b20-425a-8adf-38e665fb6275">sockaddr</a> type is used to interpret a pointer as either <b>sockaddr_in</b> or <b>sockaddr_in6</b>.




## -see-also




<a href="https://msdn.microsoft.com/6e807cc3-f9de-4d15-b337-4a6b4be910c2">SOCKET_PEER_TARGET_NAME</a>



<a href="https://msdn.microsoft.com/90439ff6-e6a8-4124-b280-a65b9ca12787">SOCKET_SECURITY_QUERY_INFO</a>



<a href="https://msdn.microsoft.com/cd222287-c4f2-4c4b-8b5f-81b6fcbe87d4">SOCKET_SECURITY_QUERY_TEMPLATE</a>



<a href="https://msdn.microsoft.com/9c47efb4-dd3e-4db9-a659-003292e2c5e9">SOCKET_SECURITY_SETTINGS</a>



<a href="https://msdn.microsoft.com/99af6ebd-6a7d-4753-8bc6-cfd42919843e">SOCKET_SECURITY_SETTINGS_IPSEC</a>



<a href="https://msdn.microsoft.com/d5e2f9d0-c61f-42d3-b62b-6c75b221ae24">Using Secure Socket Extensions</a>



<a href="https://msdn.microsoft.com/fda7738f-b7fc-49c3-aa40-9beea31d1009">WSAQuerySocketSecurity</a>



<a href="https://msdn.microsoft.com/c293658c-d7f9-411d-b6c1-a333592a741c">WSASetSocketPeerTargetName</a>



<a href="https://msdn.microsoft.com/9efee804-9763-4456-97a3-6eb9a8e30f49">WSASetSocketSecurity</a>



<a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Filtering Platform</a>



<a href="https://msdn.microsoft.com/26a69710-9981-40a4-8b1e-dca709624ead">Windows Filtering Platform  API  Functions</a>



<a href="https://msdn.microsoft.com/023a9f96-814f-40c3-a186-ae0a0c9baef2">Winsock Secure Socket Extensions</a>



<a href="https://msdn.microsoft.com/d1392e1c-2b20-425a-8adf-38e665fb6275">sockaddr</a>
 

 

