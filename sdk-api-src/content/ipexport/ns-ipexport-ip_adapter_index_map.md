---
UID: NS:ipexport._IP_ADAPTER_INDEX_MAP
title: IP_ADAPTER_INDEX_MAP (ipexport.h)
description: The IP_ADAPTER_INDEX_MAP structure stores the interface index associated with a network adapter with IPv4 enabled together with the name of the network adapter.
helpviewer_keywords: ["*PIP_ADAPTER_INDEX_MAP","IP_ADAPTER_INDEX_MAP","IP_ADAPTER_INDEX_MAP structure [IP Helper]","PIP_ADAPTER_INDEX_MAP","PIP_ADAPTER_INDEX_MAP structure pointer [IP Helper]","_iphlp_ip_adapter_index_map","ipexport/IP_ADAPTER_INDEX_MAP","ipexport/PIP_ADAPTER_INDEX_MAP","iphlp.ip_adapter_index_map"]
old-location: iphlp\ip_adapter_index_map.htm
tech.root: IpHlp
ms.assetid: 83d95ef3-13a4-4124-84cd-3016e9fb4446
ms.date: 12/05/2018
ms.keywords: '*PIP_ADAPTER_INDEX_MAP, IP_ADAPTER_INDEX_MAP, IP_ADAPTER_INDEX_MAP structure [IP Helper], PIP_ADAPTER_INDEX_MAP, PIP_ADAPTER_INDEX_MAP structure pointer [IP Helper], _iphlp_ip_adapter_index_map, ipexport/IP_ADAPTER_INDEX_MAP, ipexport/PIP_ADAPTER_INDEX_MAP, iphlp.ip_adapter_index_map'
req.header: ipexport.h
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
req.typenames: IP_ADAPTER_INDEX_MAP, *PIP_ADAPTER_INDEX_MAP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IP_ADAPTER_INDEX_MAP
 - ipexport/_IP_ADAPTER_INDEX_MAP
 - PIP_ADAPTER_INDEX_MAP
 - ipexport/PIP_ADAPTER_INDEX_MAP
 - IP_ADAPTER_INDEX_MAP
 - ipexport/IP_ADAPTER_INDEX_MAP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ipexport.h
api_name:
 - IP_ADAPTER_INDEX_MAP
---

# IP_ADAPTER_INDEX_MAP structure


## -description

The 
<b>IP_ADAPTER_INDEX_MAP</b> structure stores the interface index associated with a network adapter with IPv4 enabled together with the name of the network adapter.

## -struct-fields

### -field Index

The interface index associated with the network adapter.

### -field Name

A pointer to a Unicode string that contains the name of the adapter.

## -remarks

The 
<b>IP_ADAPTER_INDEX_MAP</b> structure is specific to network adapters with IPv4 enabled. 

An adapter index  may change when the adapter is disabled and then enabled, or under other circumstances, and should not be considered persistent.

On Windows Vista and later, the <b>Name</b> member of the <b>IP_ADAPTER_INDEX_MAP</b> structure may be a Unicode string of the GUID for the network interface (the string begins with the '{' character). 

This structure is defined in the <i>Ipexport.h</i> header file which is automatically included in the <i>Iphlpapi.h</i> header file. The <i>Ipexport.h</i> header file should never be used directly.

## -see-also

<a href="/windows/desktop/IpHlp/ip-helper-structures">IP Helper
  Structures</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start
  Page</a>



<a href="/windows/desktop/api/ipexport/ns-ipexport-ip_interface_info">IP_INTERFACE_INFO</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-ipreleaseaddress">IpReleaseAddress</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-iprenewaddress">IpRenewAddress</a>