---
UID: NS:ws2ipdef.group_source_req
title: GROUP_SOURCE_REQ (ws2ipdef.h)
description: Provides multicast group information for IPv6 or IPv4 addresses that includes the source IP address.
helpviewer_keywords: ["*PGROUP_SOURCE_REQ","GROUP_SOURCE_REQ","GROUP_SOURCE_REQ structure [Winsock]","PGROUP_SOURCE_REQ","PGROUP_SOURCE_REQ structure pointer [Winsock]","winsock.group_source_req","ws2ipdef/GROUP_SOURCE_REQ","ws2ipdef/PGROUP_SOURCE_REQ"]
old-location: winsock\group_source_req.htm
tech.root: WinSock
ms.assetid: c8f442e0-e7c3-4421-a664-3f4e31a68eb9
ms.date: 12/05/2018
ms.keywords: '*PGROUP_SOURCE_REQ, GROUP_SOURCE_REQ, GROUP_SOURCE_REQ structure [Winsock], PGROUP_SOURCE_REQ, PGROUP_SOURCE_REQ structure pointer [Winsock], winsock.group_source_req, ws2ipdef/GROUP_SOURCE_REQ, ws2ipdef/PGROUP_SOURCE_REQ'
req.header: ws2ipdef.h
req.include-header: Ws2tcpip.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.typenames: GROUP_SOURCE_REQ, *PGROUP_SOURCE_REQ
req.redist: 
ms.custom: 19H1
f1_keywords:
 - group_source_req
 - ws2ipdef/group_source_req
 - PGROUP_SOURCE_REQ
 - ws2ipdef/PGROUP_SOURCE_REQ
 - GROUP_SOURCE_REQ
 - ws2ipdef/GROUP_SOURCE_REQ
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ws2ipdef.h
api_name:
 - GROUP_SOURCE_REQ
---

# GROUP_SOURCE_REQ structure


## -description

The <b>GROUP_SOURCE_REQ</b> structure provides multicast group information for IPv6 or IPv4 addresses that includes the source IP address.

## -struct-fields

### -field gsr_interface

The interface index of the local interface on which the multicast group should be joined, dropped, blocked, or unblocked.

### -field gsr_group

The address of the multicast group. This may be either an IPv6 or IPv4 multicast address.

### -field gsr_source

The source address that should be used. This may be either an IPv6 or IPv4 multicast address, but it must be the same address family (IPv6 or IPv4) as the address specified in the <b>gsr_group</b> member.

## -remarks

The <b>GROUP_SOURCE_REQ</b> structure is used with either IPv6 or IPv4 multicast addresses. The <b>GROUP_SOURCE_REQ</b> structure is used with the <a href="/windows/desktop/WinSock/socket-options">MCAST_BLOCK_SOURCE</a>,  MCAST_JOIN_SOURCE_GROUP, MCAST_LEAVE_SOURCE_GROUP, and MCAST_UNBLOCK_SOURCE socket options. 

The <b>GROUP_SOURCE_REQ</b> structure and related structures used for multicast programming are based on IETF recommendations in sections 5 and 8.2  of RFC 3768. For more information, see <a href="http://tools.ietf.org/html/rfc3678">http://www.ietf.org/rfc/rfc3678.txt</a>.

On Windows Vista and later, a set of socket options are available for multicast programming that support IPv6 and IPv4 addresses. These socket options are IP agnostic and can be used on both IPv6 and IPv4. These IP agnostic options use the <a href="/windows/desktop/api/ws2ipdef/ns-ws2ipdef-group_req">GROUP_REQ</a> and the <b>GROUP_SOURCE_REQ</b> structures and are the preferred socket options for multicast programming on Windows Vista and later.

The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses">GetAdaptersAddresses</a> function can be used to obtain interface index information required for the <i>gsr_interface</i> member.

The <b>GROUP_SOURCE_REQ</b> structure and the socket options that use this structure are only valid on datagram and raw sockets (the socket type must be <b>SOCK_DGRAM</b> or <b>SOCK_RAW</b>).

The <b>GROUP_SOURCE_REQ</b> structure is defined in the <i>Ws2ipdef.h</i> header file which is automatically included in the <i>Ws2tcpip.h</i> header file. The <i>Ws2ipdef.h</i>  header files should never be used directly.

## -see-also

<a href="/windows/desktop/api/ws2ipdef/ns-ws2ipdef-group_filter">GROUP_FILTER</a>



<a href="/windows/desktop/api/ws2ipdef/ns-ws2ipdef-group_req">GROUP_REQ</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses">GetAdaptersAddresses</a>



<a href="/windows/desktop/WinSock/multicast-programming">Multicast Programming</a>



<a href="/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)">SOCKADDR_STORAGE</a>



<a href="/windows/desktop/WinSock/socket-options">Socket Options</a>



<a href="/windows/desktop/api/ws2ipdef/ns-ws2ipdef-ip_mreq">ip_mreq</a>



<a href="/windows/desktop/api/ws2ipdef/ns-ws2ipdef-ipv6_mreq">ipv6_mreq</a>