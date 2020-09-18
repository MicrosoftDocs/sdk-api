---
UID: NS:iptypes._IP_PER_ADAPTER_INFO_W2KSP1
title: IP_PER_ADAPTER_INFO_W2KSP1 (iptypes.h)
description: The IP_PER_ADAPTER_INFO structure contains information specific to a particular adapter.
helpviewer_keywords: ["*PIP_PER_ADAPTER_INFO","*PIP_PER_ADAPTER_INFO_W2KSP1","IP_PER_ADAPTER_INFO","IP_PER_ADAPTER_INFO structure [IP Helper]","IP_PER_ADAPTER_INFO_W2KSP1","PIP_PER_ADAPTER_INFO","PIP_PER_ADAPTER_INFO structure pointer [IP Helper]","_iphlp_ip_per_adapter_info","iphlp.ip_per_adapter_info","iptypes/IP_PER_ADAPTER_INFO","iptypes/PIP_PER_ADAPTER_INFO"]
old-location: iphlp\ip_per_adapter_info.htm
tech.root: IpHlp
ms.assetid: 10cfdded-4184-4d34-9ccd-85446c13d497
ms.date: 12/05/2018
ms.keywords: '*PIP_PER_ADAPTER_INFO, *PIP_PER_ADAPTER_INFO_W2KSP1, IP_PER_ADAPTER_INFO, IP_PER_ADAPTER_INFO structure [IP Helper], IP_PER_ADAPTER_INFO_W2KSP1, PIP_PER_ADAPTER_INFO, PIP_PER_ADAPTER_INFO structure pointer [IP Helper], _iphlp_ip_per_adapter_info, iphlp.ip_per_adapter_info, iptypes/IP_PER_ADAPTER_INFO, iptypes/PIP_PER_ADAPTER_INFO'
req.header: iptypes.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: IP_PER_ADAPTER_INFO_W2KSP1, *PIP_PER_ADAPTER_INFO_W2KSP1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IP_PER_ADAPTER_INFO_W2KSP1
 - iptypes/_IP_PER_ADAPTER_INFO_W2KSP1
 - PIP_PER_ADAPTER_INFO_W2KSP1
 - iptypes/PIP_PER_ADAPTER_INFO_W2KSP1
 - IP_PER_ADAPTER_INFO_W2KSP1
 - iptypes/IP_PER_ADAPTER_INFO_W2KSP1
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
 - IP_PER_ADAPTER_INFO
---

# IP_PER_ADAPTER_INFO_W2KSP1 structure


## -description

The 
<b>IP_PER_ADAPTER_INFO</b> structure contains information specific to a particular adapter.

## -struct-fields

### -field AutoconfigEnabled

Specifies whether IP address auto-configuration (APIPA) is enabled on this adapter. See Remarks.

### -field AutoconfigActive

Specifies whether this adapter's IP address is currently auto-configured by APIPA.

### -field CurrentDnsServer

Reserved. Use the <b>DnsServerList</b> member to obtain the DNS servers for the local computer.

### -field DnsServerList

A linked list of 
<a href="/windows/desktop/api/iptypes/ns-iptypes-ip_addr_string">IP_ADDR_STRING</a> structures that specify the set of DNS servers used by the local computer.

## -remarks

APIPA enables automatic IP address configuration on networks without DHCP servers, using the IANA-reserved Class B network 169.254.0.0, with a subnet mask of 255.255.0.0. Clients send ARP messages to ensure the selected address is not currently in use. Clients auto-configured in this fashion continue to poll for a valid DHCP server every five minutes, and if found, the DHCP server configuration overrides all auto-configuration settings.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getperadapterinfo">GetPerAdapterInfo</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/windows/desktop/IpHlp/ip-helper-structures">IP Helper Structures</a>



<a href="/windows/desktop/api/iptypes/ns-iptypes-ip_addr_string">IP_ADDR_STRING</a>