---
UID: NS:ipexport._IP_UNIDIRECTIONAL_ADAPTER_ADDRESS
title: IP_UNIDIRECTIONAL_ADAPTER_ADDRESS (ipexport.h)
description: The IP_UNIDIRECTIONAL_ADAPTER_ADDRESS structure stores the IPv4 addresses associated with a unidirectional adapter.
helpviewer_keywords: ["*PIP_UNIDIRECTIONAL_ADAPTER_ADDRESS","IP_UNIDIRECTIONAL_ADAPTER_ADDRESS","IP_UNIDIRECTIONAL_ADAPTER_ADDRESS structure [IP Helper]","PIP_UNIDIRECTIONAL_ADAPTER_ADDRESS","PIP_UNIDIRECTIONAL_ADAPTER_ADDRESS structure pointer [IP Helper]","_iphlp_ip_unidirectional_adapter_address","ipexport/IP_UNIDIRECTIONAL_ADAPTER_ADDRESS","ipexport/PIP_UNIDIRECTIONAL_ADAPTER_ADDRESS","iphlp.ip_unidirectional_adapter_address"]
old-location: iphlp\ip_unidirectional_adapter_address.htm
tech.root: IpHlp
ms.assetid: 225b93ae-e34f-4e5b-a699-1fdd342265c6
ms.date: 12/05/2018
ms.keywords: '*PIP_UNIDIRECTIONAL_ADAPTER_ADDRESS, IP_UNIDIRECTIONAL_ADAPTER_ADDRESS, IP_UNIDIRECTIONAL_ADAPTER_ADDRESS structure [IP Helper], PIP_UNIDIRECTIONAL_ADAPTER_ADDRESS, PIP_UNIDIRECTIONAL_ADAPTER_ADDRESS structure pointer [IP Helper], _iphlp_ip_unidirectional_adapter_address, ipexport/IP_UNIDIRECTIONAL_ADAPTER_ADDRESS, ipexport/PIP_UNIDIRECTIONAL_ADAPTER_ADDRESS, iphlp.ip_unidirectional_adapter_address'
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
req.typenames: IP_UNIDIRECTIONAL_ADAPTER_ADDRESS, *PIP_UNIDIRECTIONAL_ADAPTER_ADDRESS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IP_UNIDIRECTIONAL_ADAPTER_ADDRESS
 - ipexport/_IP_UNIDIRECTIONAL_ADAPTER_ADDRESS
 - PIP_UNIDIRECTIONAL_ADAPTER_ADDRESS
 - ipexport/PIP_UNIDIRECTIONAL_ADAPTER_ADDRESS
 - IP_UNIDIRECTIONAL_ADAPTER_ADDRESS
 - ipexport/IP_UNIDIRECTIONAL_ADAPTER_ADDRESS
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
 - IP_UNIDIRECTIONAL_ADAPTER_ADDRESS
---

# IP_UNIDIRECTIONAL_ADAPTER_ADDRESS structure


## -description

The 
<b>IP_UNIDIRECTIONAL_ADAPTER_ADDRESS</b> structure stores the IPv4 addresses associated with a unidirectional adapter.

## -struct-fields

### -field NumAdapters

The number of IPv4 addresses pointed to by the <b>Address</b> member.

### -field Address

An array of variables of type <a href="/windows/desktop/api/inaddr/ns-inaddr-in_addr">IPAddr</a>. Each element of the array specifies an IPv4 address associated with this unidirectional adapter.

## -remarks

The <b>IP_UNIDIRECTIONAL_ADAPTER_ADDRESS</b> structure is retrieved by the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getunidirectionaladapterinfo">GetUnidirectionalAdapterInfo</a> function. A unidirectional adapter is an adapter that can receive
    IPv4 datagrams, but can't transmit them.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getunidirectionaladapterinfo">GetUnidirectionalAdapterInfo</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/windows/desktop/IpHlp/ip-helper-structures">IP Helper Structures</a>



<a href="/windows/desktop/api/inaddr/ns-inaddr-in_addr">IPAddr</a>