---
UID: NS:mstcpip._SOCKET_SECURITY_QUERY_TEMPLATE
title: SOCKET_SECURITY_QUERY_TEMPLATE (mstcpip.h)
author: windows-sdk-content
description: Contains the security template used by the WSAQuerySocketSecurity function.
old-location: winsock\socket_security_query_template.htm
tech.root: WinSock
ms.assetid: cd222287-c4f2-4c4b-8b5f-81b6fcbe87d4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SOCKET_SECURITY_QUERY_TEMPLATE, SOCKET_SECURITY_QUERY_TEMPLATE structure [Winsock], mstcpip/SOCKET_SECURITY_QUERY_TEMPLATE, winsock.socket_security_query_template
ms.topic: struct
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
 - SOCKET_SECURITY_QUERY_TEMPLATE
product: Windows
targetos: Windows
req.typenames: SOCKET_SECURITY_QUERY_TEMPLATE
req.redist: 
---

# SOCKET_SECURITY_QUERY_TEMPLATE structure


## -description


The <b>SOCKET_SECURITY_QUERY_TEMPLATE</b> structure contains the security template used by the <a href="https://msdn.microsoft.com/fda7738f-b7fc-49c3-aa40-9beea31d1009">WSAQuerySocketSecurity</a> function.


## -struct-fields




### -field SecurityProtocol

A <a href="https://msdn.microsoft.com/ae77ac61-5035-401e-a4b6-345c1be7b2b7">SOCKET_SECURITY_PROTOCOL</a> value that identifies the protocol used to secure the traffic.


### -field PeerAddress

The IP address of the peer for which security information is being queried.  For connection-oriented sockets (protocol of <b>IPPROTO_TCP</b>), the connected socket uniquely identifies a peer.  In this case, this parameter is ignored.


### -field PeerTokenAccessMask

The access mask used for opening the peer user application and computer token handles that are returned as part of the query information.


## -remarks



The <b>SOCKET_SECURITY_QUERY_TEMPLATE</b> structure  is supported on Windows Vistaand later.

The <b>SOCKET_SECURITY_QUERY_TEMPLATE</b> structure  is used by the <a href="https://msdn.microsoft.com/fda7738f-b7fc-49c3-aa40-9beea31d1009">WSAQuerySocketSecurity</a> function to specify the type of query information to return for a socket. The <b>SOCKET_SECURITY_QUERY_TEMPLATE</b> structure passed to the <b>WSAQuerySocketSecurity</b> function may contain zeros for all members to request default security information. 

If the <b>SOCKET_SECURITY_QUERY_TEMPLATE</b> structure  is specified with the <b>PeerTokenAccessMask</b> member not specified (set to zero), then the <a href="https://msdn.microsoft.com/fda7738f-b7fc-49c3-aa40-9beea31d1009">WSAQuerySocketSecurity</a> function will not return the <b>PeerApplicationAccessTokenHandle</b> and <b>PeerMachineAccessTokenHandle</b> members in the <a href="https://msdn.microsoft.com/90439ff6-e6a8-4124-b280-a65b9ca12787">SOCKET_SECURITY_QUERY_INFO</a> structure.

Currently, the only type of security protocol that is supported is IPsec. So specifying an enumeration value  of <b>SOCKET_SECURITY_PROTOCOL_DEFAULT</b> for the <b>SecurityProtocol</b> member has the same effect as specifying <b>SOCKET_SECURITY_PROTOCOL_IPSEC</b>. 




## -see-also




<a href="https://msdn.microsoft.com/ae77ac61-5035-401e-a4b6-345c1be7b2b7">SOCKET_SECURITY_PROTOCOL</a>



<a href="https://msdn.microsoft.com/90439ff6-e6a8-4124-b280-a65b9ca12787">SOCKET_SECURITY_QUERY_INFO</a>



<a href="https://msdn.microsoft.com/d5e2f9d0-c61f-42d3-b62b-6c75b221ae24">Using Secure Socket Extensions</a>



<a href="https://msdn.microsoft.com/fda7738f-b7fc-49c3-aa40-9beea31d1009">WSAQuerySocketSecurity</a>



<a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Filtering Platform</a>



<a href="https://msdn.microsoft.com/26a69710-9981-40a4-8b1e-dca709624ead">Windows Filtering Platform  API  Functions</a>



<a href="https://msdn.microsoft.com/023a9f96-814f-40c3-a186-ae0a0c9baef2">Winsock Secure Socket Extensions</a>
 

 

