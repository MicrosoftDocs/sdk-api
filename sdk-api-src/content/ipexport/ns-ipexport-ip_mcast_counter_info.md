---
UID: NS:ipexport._IP_MCAST_COUNTER_INFO
title: IP_MCAST_COUNTER_INFO (ipexport.h)
description: The IP_MCAST_COUNTER_INFO structure stores statistical information about Multicast traffic.
helpviewer_keywords: ["*PIP_MCAST_COUNTER_INFO","*PIP_MCAST_COUNTER_INFO structure [IP Helper]","IP_MCAST_COUNTER_INFO","IP_MCAST_COUNTER_INFO structure [IP Helper]","ipexport/*PIP_MCAST_COUNTER_INFO","ipexport/IP_MCAST_COUNTER_INFO","iphlp.ip_mcast_counter_info"]
old-location: iphlp\ip_mcast_counter_info.htm
tech.root: IpHlp
ms.assetid: aa70f260-ccbb-4020-a3c0-2d400ddc2e9d
ms.date: 12/05/2018
ms.keywords: '*PIP_MCAST_COUNTER_INFO, *PIP_MCAST_COUNTER_INFO structure [IP Helper], IP_MCAST_COUNTER_INFO, IP_MCAST_COUNTER_INFO structure [IP Helper], ipexport/*PIP_MCAST_COUNTER_INFO, ipexport/IP_MCAST_COUNTER_INFO, iphlp.ip_mcast_counter_info'
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
req.typenames: IP_MCAST_COUNTER_INFO, *PIP_MCAST_COUNTER_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IP_MCAST_COUNTER_INFO
 - ipexport/_IP_MCAST_COUNTER_INFO
 - PIP_MCAST_COUNTER_INFO
 - ipexport/PIP_MCAST_COUNTER_INFO
 - IP_MCAST_COUNTER_INFO
 - ipexport/IP_MCAST_COUNTER_INFO
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
 - IP_MCAST_COUNTER_INFO
---

# IP_MCAST_COUNTER_INFO structure


## -description

The <b>IP_MCAST_COUNTER_INFO</b> structure stores statistical information about Multicast traffic.

## -struct-fields

### -field InMcastOctets

The number of  multicast octets received.

### -field OutMcastOctets

The number of  multicast octets transmitted.

### -field InMcastPkts

The number of multicast packets received.

### -field OutMcastPkts

The number of multicast packets transmitted.

## -remarks

This structure is defined in the <i>Ipexport.h</i> header file which is automatically included in the <i>Iphlpapi.h</i> header file. The <i>Ipexport.h</i> header file should never be used directly.

## -see-also

<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/windows/desktop/IpHlp/ip-helper-structures">IP Helper Structures</a>