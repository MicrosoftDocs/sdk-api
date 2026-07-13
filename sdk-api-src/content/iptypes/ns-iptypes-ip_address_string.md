---
UID: NS:iptypes.IP_ADDRESS_STRING
title: IP_ADDRESS_STRING (iptypes.h)
description: Stores an IPv4 address in dotted decimal notation.
helpviewer_keywords: ["*PIP_ADDRESS_STRING","*PIP_ADDRESS_STRING","IP_MASK_STRING","*PIP_MASK_STRING","*PIP_ADDRESS_STRING","IP_MASK_STRING","*PIP_MASK_STRING structure [IP Helper]","*PIP_MASK_STRING","IP_ADDRESS_STRING","IP_ADDRESS_STRING structure [IP Helper]","IP_MASK_STRING","iphlp.ip_address_string","iptypes/*PIP_ADDRESS_STRING","IP_MASK_STRING","*PIP_MASK_STRING","iptypes/IP_ADDRESS_STRING"]
old-location: iphlp\ip_address_string.htm
tech.root: IpHlp
ms.assetid: f426b22f-66e4-43e4-8852-357359df6f88
ms.date: 12/05/2018
ms.keywords: '*PIP_ADDRESS_STRING, *PIP_ADDRESS_STRING,IP_MASK_STRING,*PIP_MASK_STRING, *PIP_ADDRESS_STRING,IP_MASK_STRING,*PIP_MASK_STRING structure [IP Helper], *PIP_MASK_STRING, IP_ADDRESS_STRING, IP_ADDRESS_STRING structure [IP Helper], IP_MASK_STRING, iphlp.ip_address_string, iptypes/*PIP_ADDRESS_STRING,IP_MASK_STRING,*PIP_MASK_STRING, iptypes/IP_ADDRESS_STRING'
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
req.typenames: IP_ADDRESS_STRING, *PIP_ADDRESS_STRING, IP_MASK_STRING, *PIP_MASK_STRING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PIP_ADDRESS_STRING
 - iptypes/PIP_ADDRESS_STRING
 - IP_ADDRESS_STRING
 - iptypes/IP_ADDRESS_STRING
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
 - IP_ADDRESS_STRING
---

# IP_ADDRESS_STRING structure


## -description

The <b>IP_ADDRESS_STRING</b> structure stores an IPv4 address in dotted decimal notation. The <b>IP_ADDRESS_STRING</b> structure definition is also the type definition for the <b>IP_MASK_STRING</b> structure.

## -struct-fields

### -field String

A character string that represents an IPv4 address or an IPv4 subnet mask in dotted decimal notation.

## -remarks

The <b>IP_ADDRESS_STRING</b> structure is used as  a parameter in  the  <a href="/windows/desktop/api/iptypes/ns-iptypes-ip_addr_string">IP_ADDR_STRING</a> structure.

## -see-also

<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/windows/desktop/IpHlp/ip-helper-structures">IP Helper Structures</a>



<a href="/windows/desktop/api/iptypes/ns-iptypes-ip_addr_string">IP_ADDR_STRING</a>

