---
UID: NS:ws2ipdef.ip_mreq
title: IP_MREQ (ws2ipdef.h)
description: The ip_mreq structure provides multicast group information for IPv4 addresses.
helpviewer_keywords: ["*PIP_MREQ","IP_MREQ","IP_MREQ [Winsock]","IP_MREQ structure [Winsock]","PIP_MREQ","PIP_MREQ structure pointer [Winsock]","ip_mreq","ip_mreq structure [Winsock]","winsock.ip_mreq","ws2ipdef/PIP_MREQ","ws2ipdef/ip_mreq","ws2tcpip/PIP_MREQ","ws2tcpip/ip_mreq"]
old-location: winsock\ip_mreq.htm
tech.root: WinSock
ms.assetid: 0bcf4c17-679d-42fc-b77e-722ce955d01f
ms.date: 12/05/2018
ms.keywords: '*PIP_MREQ, IP_MREQ, IP_MREQ [Winsock], IP_MREQ structure [Winsock], PIP_MREQ, PIP_MREQ structure pointer [Winsock], ip_mreq, ip_mreq structure [Winsock], winsock.ip_mreq, ws2ipdef/PIP_MREQ, ws2ipdef/ip_mreq, ws2tcpip/PIP_MREQ, ws2tcpip/ip_mreq'
req.header: ws2ipdef.h
req.include-header: Ws2tcpip.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: IP_MREQ, *PIP_MREQ
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ip_mreq
 - ws2ipdef/ip_mreq
 - PIP_MREQ
 - ws2ipdef/PIP_MREQ
 - IP_MREQ
 - ws2ipdef/IP_MREQ
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ws2ipdef.h
 - Ws2tcpip.h
api_name:
 - IP_MREQ
---

# IP_MREQ structure


## -description

The <b>ip_mreq</b> structure provides multicast group information for IPv4 addresses.

## -struct-fields

### -field imr_multiaddr

The address of the IPv4 multicast group.

### -field imr_interface

The local IPv4 address of the interface or the interface index on which the multicast group should be joined or dropped. This value is in network byte order. If this member specifies an IPv4 address of 0.0.0.0, the default IPv4 multicast interface is used. 

 To use an interface index of 1 would be the same as an IP address of  0.0.0.1.

## -remarks

The <b>ip_mreq</b> structure is used with IPv4 addresses. The <b>ip_mreq</b> structure is used with the <a href="/windows/desktop/WinSock/ipproto-ip-socket-options">IP_ADD_MEMBERSHIP</a> and <b>IP_DROP_MEMBERSHIP</b> socket options. 

The <b>ip_mreq</b> structure and related structures used for IPv4 multicast programming are based on IETF recommendations in sections 4 and 8.1 of RFC 3768. For more information, see <a href="http://tools.ietf.org/html/rfc3678">http://www.ietf.org/rfc/rfc3678.txt</a>.

For more configurable multicast capabilities with IPv4, use the <a href="/windows/desktop/api/ws2ipdef/ns-ws2ipdef-ip_mreq_source">ip_mreq_source</a> structure. See <a href="/windows/desktop/WinSock/multicast-programming">Multicast Programming</a> for more information. 

On Windows Vista and later, a set of socket options are available for multicast programming that support IPv6 and IPv4 addresses. These socket options are IP agnostic and can be used on both IPv6 and IPv4. These IP agnostic options use the <a href="/windows/desktop/api/ws2ipdef/ns-ws2ipdef-group_req">GROUP_REQ</a> and the <a href="/windows/desktop/api/ws2ipdef/ns-ws2ipdef-group_source_req">GROUP_SOURCE_REQ</a> structures and are the preferred socket options for multicast programming on Windows Vista and later.

The <b>ip_mreq</b> structure is the IPv4 equivalent of the IPv6-based <a href="/windows/desktop/api/ws2ipdef/ns-ws2ipdef-ipv6_mreq">ipv6_mreq</a> structure.  

The <b>imr_interface</b> member can be an interface index. Any IP address in the 0.x.x.x block (first octet of 0) except for the IP address of 0.0.0.0 is treated as an interface index.
An interface index is a 24-bit number. The 0.0.0.0/8 IPv4 address block is not used (this range is reserved). The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses">GetAdaptersAddresses</a> function can be used to obtain interface index information to use for the <b>imr_interface</b> member.

It is recommended that a local IPv4 address or interface index always be specified in the <b>imr_interface</b> member of the <b>ip_mreq</b> structure, rather than use the default interface.  This is particularly important on computers with multiple network interfaces and multiple public IPv4 addresses. 

The default interface used for IPv4 multicast is  determined by the networking stack in Windows. An application can determine the default interface used for IPv4 multicast using the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipforwardtable">GetIpForwardTable</a> function to retrieve the IPv4 routing table. The network interface with the lowest value for the routing metric for a destination IP address of 224.0.0.0 is the default interface for IPv4 multicast. The routing table can also be displayed from the command prompt with the following command:

<b>route print</b>

The <a href="/windows/desktop/WinSock/ipproto-ip-socket-options">IP_MULTICAST_IF</a> socket option can be used to set the default interface to send IPv4 multicast packets. This socket option does not change the default interface used to receive IPv4 multicast packets.


A typical IPv4  multicast application would use the <a href="/windows/desktop/WinSock/ipproto-ip-socket-options">IP_ADD_MEMBERSHIP</a> socket option with the <b>ip_mreq</b> structure to join a multicast group and listen for multicast packets on a specific interface. The <b>IP_MULTICAST_IF</b> socket option would be used to set the interface to send IPv4 multicast packets to the multicast group. The most common scenario would be a multicast application that listens and sends on the same interface for a multicast group. Multiple sockets might be used by a multicast application with one  socket for listening and one or more sockets for sending. 

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>ip_mreq</b> structure is defined in the <i>Ws2ipdef.h</i> header file which is automatically included in the <i>Ws2tcpip.h</i> header file. The <i>Ws2ipdef.h</i>  header files should never be used directly.

<div class="alert"><b>Note</b>  The <b>IP_MREQ</b> and <b>PIP_MREQ</b> derived structures are only defined on the Windows SDK released with Windows Vista and later. The <b>ip_mreq</b> structure should be used on earlier versions of the Windows SDK. </div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/ws2ipdef/ns-ws2ipdef-group_req">GROUP_REQ</a>



<a href="/windows/desktop/api/ws2ipdef/ns-ws2ipdef-group_source_req">GROUP_SOURCE_REQ</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses">GetAdaptersAddresses</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipforwardtable">GetIpForwardTable</a>



<a href="/windows/desktop/WinSock/ipproto-ip-socket-options">IPPROTO_IP Socket Options</a>



<a href="/windows/desktop/WinSock/multicast-programming">Multicast Programming</a>



<a href="/windows/desktop/WinSock/socket-options">Socket Options</a>



<a href="/windows/desktop/api/ws2ipdef/ns-ws2ipdef-ip_mreq_source">ip_mreq_source</a>



<a href="/windows/desktop/api/ws2ipdef/ns-ws2ipdef-ip_msfilter">ip_msfilter</a>



<a href="/windows/desktop/api/ws2ipdef/ns-ws2ipdef-ipv6_mreq">ipv6_mreq</a>