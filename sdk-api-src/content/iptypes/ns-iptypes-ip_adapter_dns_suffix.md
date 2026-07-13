---
UID: NS:iptypes._IP_ADAPTER_DNS_SUFFIX
title: IP_ADAPTER_DNS_SUFFIX (iptypes.h)
description: The IP_ADAPTER_DNS_SUFFIX structure stores a DNS suffix in a linked list of DNS suffixes for a particular adapter.
helpviewer_keywords: ["*PIP_ADAPTER_DNS_SUFFIX","IP_ADAPTER_DNS_SUFFIX","IP_ADAPTER_DNS_SUFFIX structure [IP Helper]","PIP_ADAPTER_DNS_SUFFIX","PIP_ADAPTER_DNS_SUFFIX structure pointer [IP Helper]","iphlp.ip_adapter_dns_suffix","iptypes/IP_ADAPTER_DNS_SUFFIX","iptypes/PIP_ADAPTER_DNS_SUFFIX"]
old-location: iphlp\ip_adapter_dns_suffix.htm
tech.root: IpHlp
ms.assetid: 3730a406-2995-48f7-b70e-1cf8258ee4a6
ms.date: 12/05/2018
ms.keywords: '*PIP_ADAPTER_DNS_SUFFIX, IP_ADAPTER_DNS_SUFFIX, IP_ADAPTER_DNS_SUFFIX structure [IP Helper], PIP_ADAPTER_DNS_SUFFIX, PIP_ADAPTER_DNS_SUFFIX structure pointer [IP Helper], iphlp.ip_adapter_dns_suffix, iptypes/IP_ADAPTER_DNS_SUFFIX, iptypes/PIP_ADAPTER_DNS_SUFFIX'
req.header: iptypes.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
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
req.typenames: IP_ADAPTER_DNS_SUFFIX, *PIP_ADAPTER_DNS_SUFFIX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IP_ADAPTER_DNS_SUFFIX
 - iptypes/_IP_ADAPTER_DNS_SUFFIX
 - PIP_ADAPTER_DNS_SUFFIX
 - iptypes/PIP_ADAPTER_DNS_SUFFIX
 - IP_ADAPTER_DNS_SUFFIX
 - iptypes/IP_ADAPTER_DNS_SUFFIX
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
 - IP_ADAPTER_DNS_SUFFIX
---

# IP_ADAPTER_DNS_SUFFIX structure


## -description

The 
<b>IP_ADAPTER_DNS_SUFFIX</b> structure stores a DNS suffix in a linked list of DNS suffixes  for a particular adapter.

## -struct-fields

### -field Next

A pointer to the next DNS suffix in the linked list.

### -field String

The DNS suffix for this DNS suffix entry.

## -remarks

The <a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_lh">IP_ADAPTER_ADDRESSES</a> structure is retrieved by the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses">GetAdaptersAddresses</a> function. The <b>FirstDnsSuffix</b> member of the <b>IP_ADAPTER_ADDRESSES</b> structure is a pointer to a linked list of <b>IP_ADAPTER_DNS_SUFFIX</b> structures.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses">GetAdaptersAddresses</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/windows/desktop/IpHlp/ip-helper-structures">IP Helper Structures</a>



<a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_lh">IP_ADAPTER_ADDRESSES</a>