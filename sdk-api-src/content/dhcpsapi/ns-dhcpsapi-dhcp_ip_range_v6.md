---
UID: NS:dhcpsapi._DHCP_IP_RANGE_V6
title: DHCP_IP_RANGE_V6 (dhcpsapi.h)
description: Specifies a range of IPv6 addresses for use with a DHCPv6 server.
helpviewer_keywords: ["*LPDHCP_IP_RANGE_V6","DHCP_IP_RANGE_V6","DHCP_IP_RANGE_V6 structure [DHCP]","PDHCP_IP_RANGE_V6","PDHCP_IP_RANGE_V6 structure pointer [DHCP]","dhcp.dhcp_ip_range_v6","dhcpsapi/DHCP_IP_RANGE_V6","dhcpsapi/PDHCP_IP_RANGE_V6"]
old-location: dhcp\dhcp_ip_range_v6.htm
tech.root: DHCP
ms.assetid: 3a918a2b-beff-4562-9c7f-acee2cc8f2da
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_IP_RANGE_V6, DHCP_IP_RANGE_V6, DHCP_IP_RANGE_V6 structure [DHCP], PDHCP_IP_RANGE_V6, PDHCP_IP_RANGE_V6 structure pointer [DHCP], dhcp.dhcp_ip_range_v6, dhcpsapi/DHCP_IP_RANGE_V6, dhcpsapi/PDHCP_IP_RANGE_V6'
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: DHCP_IP_RANGE_V6, *LPDHCP_IP_RANGE_V6
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_IP_RANGE_V6
 - dhcpsapi/_DHCP_IP_RANGE_V6
 - LPDHCP_IP_RANGE_V6
 - dhcpsapi/LPDHCP_IP_RANGE_V6
 - DHCP_IP_RANGE_V6
 - dhcpsapi/DHCP_IP_RANGE_V6
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dhcpsapi.h
api_name:
 - DHCP_IP_RANGE_V6
---

# DHCP_IP_RANGE_V6 structure


## -description

The <b>DHCP_IP_RANGE_V6</b> structure specifies a range of IPv6 addresses for use with a DHCPv6 server.

## -struct-fields

### -field StartAddress

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_ipv6_address">DHCP_IPV6_ADDRESS</a> structure that contains the first IPv6 address in the range.

### -field EndAddress

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_ipv6_address">DHCP_IPV6_ADDRESS</a> structure that contains the last IPv6 address in the range.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_ipv6_address">DHCP_IPV6_ADDRESS</a>