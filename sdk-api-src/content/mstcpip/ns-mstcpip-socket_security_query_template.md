---
UID: NS:mstcpip._SOCKET_SECURITY_QUERY_TEMPLATE
title: SOCKET_SECURITY_QUERY_TEMPLATE (mstcpip.h)
description: Contains the security template used by the WSAQuerySocketSecurity function.
helpviewer_keywords: ["SOCKET_SECURITY_QUERY_TEMPLATE","SOCKET_SECURITY_QUERY_TEMPLATE structure [Winsock]","mstcpip/SOCKET_SECURITY_QUERY_TEMPLATE","winsock.socket_security_query_template"]
old-location: winsock\socket_security_query_template.htm
tech.root: WinSock
ms.assetid: cd222287-c4f2-4c4b-8b5f-81b6fcbe87d4
ms.date: 12/05/2018
ms.keywords: SOCKET_SECURITY_QUERY_TEMPLATE, SOCKET_SECURITY_QUERY_TEMPLATE structure [Winsock], mstcpip/SOCKET_SECURITY_QUERY_TEMPLATE, winsock.socket_security_query_template
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
targetos: Windows
req.typenames: SOCKET_SECURITY_QUERY_TEMPLATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SOCKET_SECURITY_QUERY_TEMPLATE
 - mstcpip/_SOCKET_SECURITY_QUERY_TEMPLATE
 - SOCKET_SECURITY_QUERY_TEMPLATE
 - mstcpip/SOCKET_SECURITY_QUERY_TEMPLATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mstcpip.h
api_name:
 - SOCKET_SECURITY_QUERY_TEMPLATE
---

# SOCKET_SECURITY_QUERY_TEMPLATE structure


## -description

The <b>SOCKET_SECURITY_QUERY_TEMPLATE</b> structure contains the security template used by the <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity">WSAQuerySocketSecurity</a> function.

## -struct-fields

### -field SecurityProtocol

A <a href="/windows/desktop/api/mstcpip/ne-mstcpip-socket_security_protocol">SOCKET_SECURITY_PROTOCOL</a> value that identifies the protocol used to secure the traffic.

### -field PeerAddress

The IP address of the peer for which security information is being queried.  For connection-oriented sockets (protocol of <b>IPPROTO_TCP</b>), the connected socket uniquely identifies a peer.  In this case, this parameter is ignored.

### -field PeerTokenAccessMask

The access mask used for opening the peer user application and computer token handles that are returned as part of the query information.

## -remarks

The <b>SOCKET_SECURITY_QUERY_TEMPLATE</b> structure  is supported on Windows Vista and later.

The <b>SOCKET_SECURITY_QUERY_TEMPLATE</b> structure  is used by the <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity">WSAQuerySocketSecurity</a> function to specify the type of query information to return for a socket. The <b>SOCKET_SECURITY_QUERY_TEMPLATE</b> structure passed to the <b>WSAQuerySocketSecurity</b> function may contain zeros for all members to request default security information. 

If the <b>SOCKET_SECURITY_QUERY_TEMPLATE</b> structure  is specified with the <b>PeerTokenAccessMask</b> member not specified (set to zero), then the <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity">WSAQuerySocketSecurity</a> function will not return the <b>PeerApplicationAccessTokenHandle</b> and <b>PeerMachineAccessTokenHandle</b> members in the <a href="/windows/desktop/api/mstcpip/ns-mstcpip-socket_security_query_info">SOCKET_SECURITY_QUERY_INFO</a> structure.

Currently, the only type of security protocol that is supported is IPsec. So specifying an enumeration value  of <b>SOCKET_SECURITY_PROTOCOL_DEFAULT</b> for the <b>SecurityProtocol</b> member has the same effect as specifying <b>SOCKET_SECURITY_PROTOCOL_IPSEC</b>.

## -see-also

<a href="/windows/desktop/api/mstcpip/ne-mstcpip-socket_security_protocol">SOCKET_SECURITY_PROTOCOL</a>



<a href="/windows/desktop/api/mstcpip/ns-mstcpip-socket_security_query_info">SOCKET_SECURITY_QUERY_INFO</a>



<a href="/windows/desktop/WinSock/using-secure-socket-extensions">Using Secure Socket Extensions</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity">WSAQuerySocketSecurity</a>



<a href="/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Filtering Platform</a>



<a href="/windows/desktop/FWP/fwp-functions">Windows Filtering Platform  API  Functions</a>



<a href="/windows/desktop/WinSock/winsock-secure-socket-extensions">Winsock Secure Socket Extensions</a>