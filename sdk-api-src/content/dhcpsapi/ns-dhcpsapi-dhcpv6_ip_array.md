---
UID: NS:dhcpsapi._DHCPV6_IP_ARRAY
title: DHCPV6_IP_ARRAY (dhcpsapi.h)
description: The DHCPV6_IP_ARRAY structure contains an array of DHCP IPv6 address structures.
helpviewer_keywords: ["*LPDHCPV6_IP_ARRAY","DHCPV6_IP_ARRAY","DHCPV6_IP_ARRAY structure [DHCP]","PDHCPV6_IP_ARRAY","PDHCPV6_IP_ARRAY structure pointer [DHCP]","dhcp.dhcpv6_ip_array","dhcpsapi/DHCPV6_IP_ARRAY","dhcpsapi/PDHCPV6_IP_ARRAY"]
old-location: dhcp\dhcpv6_ip_array.htm
tech.root: DHCP
ms.assetid: B87CF991-FFC8-4CB4-8EE9-66716EC9B58D
ms.date: 12/05/2018
ms.keywords: '*LPDHCPV6_IP_ARRAY, DHCPV6_IP_ARRAY, DHCPV6_IP_ARRAY structure [DHCP], PDHCPV6_IP_ARRAY, PDHCPV6_IP_ARRAY structure pointer [DHCP], dhcp.dhcpv6_ip_array, dhcpsapi/DHCPV6_IP_ARRAY, dhcpsapi/PDHCPV6_IP_ARRAY'
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: DHCPV6_IP_ARRAY, *LPDHCPV6_IP_ARRAY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCPV6_IP_ARRAY
 - dhcpsapi/_DHCPV6_IP_ARRAY
 - LPDHCPV6_IP_ARRAY
 - dhcpsapi/LPDHCPV6_IP_ARRAY
 - DHCPV6_IP_ARRAY
 - dhcpsapi/DHCPV6_IP_ARRAY
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
 - DHCPV6_IP_ARRAY
---

# DHCPV6_IP_ARRAY structure


## -description

The <b>DHCPV6_IP_ARRAY</b> structure contains an array of DHCP IPv6 address structures.

## -struct-fields

### -field NumElements

The number of elements in <b>Elements</b>.

### -field Elements

An array of <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_ipv6_address">DHCP_IPV6_ADDRESS</a> structures.

### -field Elements.size_is

### -field Elements.size_is.NumElements