---
UID: NS:dhcpsapi._DHCP_IP_RANGE_ARRAY
title: DHCP_IP_RANGE_ARRAY (dhcpsapi.h)
description: The DHCP_IP_RANGE_ARRAY structure defines an array of DHCP IPv4 ranges.
helpviewer_keywords: ["*LPDHCP_IP_RANGE_ARRAY","*PDHCP_IP_RANGE_ARRAY","DHCP_IP_RANGE_ARRAY","DHCP_IP_RANGE_ARRAY structure [DHCP]","LPDHCP_IP_RANGE_ARRAY","LPDHCP_IP_RANGE_ARRAY structure pointer [DHCP]","PDHCP_IP_RANGE_ARRAY","PDHCP_IP_RANGE_ARRAY structure pointer [DHCP]","dhcp.dhcp_ip_range_array","dhcpsapi/DHCP_IP_RANGE_ARRAY","dhcpsapi/LPDHCP_IP_RANGE_ARRAY","dhcpsapi/PDHCP_IP_RANGE_ARRAY"]
old-location: dhcp\dhcp_ip_range_array.htm
tech.root: DHCP
ms.assetid: BC6C85D6-D123-44D6-BFE4-3073EC51B7EA
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_IP_RANGE_ARRAY, *PDHCP_IP_RANGE_ARRAY, DHCP_IP_RANGE_ARRAY, DHCP_IP_RANGE_ARRAY structure [DHCP], LPDHCP_IP_RANGE_ARRAY, LPDHCP_IP_RANGE_ARRAY structure pointer [DHCP], PDHCP_IP_RANGE_ARRAY, PDHCP_IP_RANGE_ARRAY structure pointer [DHCP], dhcp.dhcp_ip_range_array, dhcpsapi/DHCP_IP_RANGE_ARRAY, dhcpsapi/LPDHCP_IP_RANGE_ARRAY, dhcpsapi/PDHCP_IP_RANGE_ARRAY'
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: DHCP_IP_RANGE_ARRAY, *PDHCP_IP_RANGE_ARRAY, *LPDHCP_IP_RANGE_ARRAY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_IP_RANGE_ARRAY
 - dhcpsapi/_DHCP_IP_RANGE_ARRAY
 - PDHCP_IP_RANGE_ARRAY
 - dhcpsapi/PDHCP_IP_RANGE_ARRAY
 - DHCP_IP_RANGE_ARRAY
 - dhcpsapi/DHCP_IP_RANGE_ARRAY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dhcpsapi.h
api_name:
 - DHCP_IP_RANGE_ARRAY
---

# DHCP_IP_RANGE_ARRAY structure


## -description

The <b>DHCP_IP_RANGE_ARRAY</b> structure defines an array of DHCP IPv4 ranges.

## -struct-fields

### -field NumElements

Integer that specifies the number of DHCP IPv4 ranges in <b>Elements.</b>

### -field Elements

Pointer to a list of <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_ip_range">DHCP_IP_RANGE</a>  structures.

### -field Elements.size_is

### -field Elements.size_is.NumElements

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_policy">DHCP_POLICY</a>