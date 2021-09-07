---
UID: NS:iptypes._IP_ADAPTER_DNS_SERVER_ADDRESS_XP
title: IP_ADAPTER_DNS_SERVER_ADDRESS_XP (iptypes.h)
description: The IP_ADAPTER_DNS_SERVER_ADDRESS structure stores a single DNS server address in a linked list of DNS server addresses for a particular adapter.
helpviewer_keywords: ["*PIP_ADAPTER_DNS_SERVER_ADDRESS","*PIP_ADAPTER_DNS_SERVER_ADDRESS_XP","IP_ADAPTER_DNS_SERVER_ADDRESS","IP_ADAPTER_DNS_SERVER_ADDRESS structure [IP Helper]","IP_ADAPTER_DNS_SERVER_ADDRESS_XP","PIP_ADAPTER_DNS_SERVER_ADDRESS","PIP_ADAPTER_DNS_SERVER_ADDRESS structure pointer [IP Helper]","_iphlp_ip_adapter_dns_server_address","iphlp.ip_adapter_dns_server_address","iptypes/IP_ADAPTER_DNS_SERVER_ADDRESS","iptypes/PIP_ADAPTER_DNS_SERVER_ADDRESS"]
old-location: iphlp\ip_adapter_dns_server_address.htm
tech.root: IpHlp
ms.assetid: 96855386-9010-40df-8260-16b43ad6646f
ms.date: 12/05/2018
ms.keywords: '*PIP_ADAPTER_DNS_SERVER_ADDRESS, *PIP_ADAPTER_DNS_SERVER_ADDRESS_XP, IP_ADAPTER_DNS_SERVER_ADDRESS, IP_ADAPTER_DNS_SERVER_ADDRESS structure [IP Helper], IP_ADAPTER_DNS_SERVER_ADDRESS_XP, PIP_ADAPTER_DNS_SERVER_ADDRESS, PIP_ADAPTER_DNS_SERVER_ADDRESS structure pointer [IP Helper], _iphlp_ip_adapter_dns_server_address, iphlp.ip_adapter_dns_server_address, iptypes/IP_ADAPTER_DNS_SERVER_ADDRESS, iptypes/PIP_ADAPTER_DNS_SERVER_ADDRESS'
req.header: iptypes.h
req.include-header: Iphlpapi.h
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
req.typenames: IP_ADAPTER_DNS_SERVER_ADDRESS_XP, *PIP_ADAPTER_DNS_SERVER_ADDRESS_XP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IP_ADAPTER_DNS_SERVER_ADDRESS_XP
 - iptypes/_IP_ADAPTER_DNS_SERVER_ADDRESS_XP
 - PIP_ADAPTER_DNS_SERVER_ADDRESS_XP
 - iptypes/PIP_ADAPTER_DNS_SERVER_ADDRESS_XP
 - IP_ADAPTER_DNS_SERVER_ADDRESS_XP
 - iptypes/IP_ADAPTER_DNS_SERVER_ADDRESS_XP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iptypes.h
api_name:
 - IP_ADAPTER_DNS_SERVER_ADDRESS
---

# IP_ADAPTER_DNS_SERVER_ADDRESS_XP structure


## -description

The 
<b>IP_ADAPTER_DNS_SERVER_ADDRESS</b> structure stores a single DNS server address in a linked list of DNS server addresses for a particular adapter.

## -struct-fields

### -field Alignment

Reserved. Used by the compiler to align the structure.

### -field Length

The length, in bytes, of this structure.

### -field Reserved

Reserved.

### -field Next

A pointer to the next DNS server address structure in the list.

### -field Address

The IP address for this DNS server entry. This member can be an IPv6 address or an IPv4 address.

## -remarks

The <a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_lh">IP_ADAPTER_ADDRESSES</a> structure is retrieved by the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses">GetAdaptersAddresses</a> function. The <b>FirstDnsServerAddress</b> member of the <b>IP_ADAPTER_ADDRESSES</b> structure is a pointer to a linked list of <b>IP_ADAPTER_DNS_SERVER_ADDRESS</b> structures. 

The <a href="/windows/desktop/api/ws2def/ns-ws2def-socket_address">SOCKET_ADDRESS</a> structure is used in the <b>IP_ADAPTER_DNS_SERVER_ADDRESS</b> structure. On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>SOCKET_ADDRESS</b> structure is defined in the <i>Ws2def.h</i> header file which is automatically included by the <i>Winsock2.h</i> header file. On the Platform Software Development Kit (SDK) released for Windows Server 2003 and Windows XP, the <b>SOCKET_ADDRESS</b> structure is declared in the <i>Winsock2.h</i> header file. In order to use the <b>IP_ADAPTER_DNS_SERVER_ADDRESS</b> structure, the <i>Winsock2.h</i> header file must be included before the <i>Iphlpapi.h</i> header file.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses">GetAdaptersAddresses</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/windows/desktop/IpHlp/ip-helper-structures">IP Helper Structures</a>



<a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_lh">IP_ADAPTER_ADDRESSES</a>



<a href="/windows/desktop/api/ws2def/ns-ws2def-socket_address">SOCKET_ADDRESS</a>