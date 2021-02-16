---
UID: NS:ipexport._IP_ADAPTER_ORDER_MAP
title: IP_ADAPTER_ORDER_MAP (ipexport.h)
description: The IP_ADAPTER_ORDER_MAP structure stores an array of information about adapters and their relative priority on the local computer.
helpviewer_keywords: ["*PIP_ADAPTER_ORDER_MAP","IP_ADAPTER_ORDER_MAP","IP_ADAPTER_ORDER_MAP structure [IP Helper]","PIP_ADAPTER_ORDER_MAP","PIP_ADAPTER_ORDER_MAP structure pointer [IP Helper]","ipexport/IP_ADAPTER_ORDER_MAP","ipexport/PIP_ADAPTER_ORDER_MAP","iphlp.ip_adapter_order_map"]
old-location: iphlp\ip_adapter_order_map.htm
tech.root: IpHlp
ms.assetid: 0bbd008e-67d4-4557-bff7-f0404a8878ff
ms.date: 12/05/2018
ms.keywords: '*PIP_ADAPTER_ORDER_MAP, IP_ADAPTER_ORDER_MAP, IP_ADAPTER_ORDER_MAP structure [IP Helper], PIP_ADAPTER_ORDER_MAP, PIP_ADAPTER_ORDER_MAP structure pointer [IP Helper], ipexport/IP_ADAPTER_ORDER_MAP, ipexport/PIP_ADAPTER_ORDER_MAP, iphlp.ip_adapter_order_map'
req.header: ipexport.h
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
req.typenames: IP_ADAPTER_ORDER_MAP, *PIP_ADAPTER_ORDER_MAP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IP_ADAPTER_ORDER_MAP
 - ipexport/_IP_ADAPTER_ORDER_MAP
 - PIP_ADAPTER_ORDER_MAP
 - ipexport/PIP_ADAPTER_ORDER_MAP
 - IP_ADAPTER_ORDER_MAP
 - ipexport/IP_ADAPTER_ORDER_MAP
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
 - IP_ADAPTER_ORDER_MAP
---

# IP_ADAPTER_ORDER_MAP structure


## -description

The <b>IP_ADAPTER_ORDER_MAP</b> structure stores an array of information about adapters and their relative priority on the local computer.

## -struct-fields

### -field NumAdapters

The number of network adapters in the <b>AdapterOrder</b> member.

### -field AdapterOrder

An array of adapter indexes  on the local computer, provided in the order specified in the <b>Adapters and Bindings</b> dialog box for <b>Network Connections</b>.

## -remarks

This structure is returned by the GetAdapterOrderMap function, and is used as a tie breaker for otherwise equal interfaces during network operations. The GetAdapterOrderMap function should not be called directly; use the GetAdaptersInfo function instead.

The <b>IP_ADAPTER_ORDER_MAP</b> structure contains at least one <b>AdapterOrder</b> member even if the <b>NumAdapters</b> member of the <b>IP_ADAPTER_ORDER_MAP</b> structure indicates no network adapters. When the <b>NumAdapters</b> member of the <b>IP_ADAPTER_ORDER_MAP</b> structure is zero, the value of the single  <b>AdapterOrder</b> member is undefined. 

This structure is defined in the <i>Ipexport.h</i> header file which is automatically included in the <i>Iphlpapi.h</i> header file. The <i>Ipexport.h</i> header file should never be used directly.

## -see-also

GetAdapterOrderMap



GetAdaptersInfo

