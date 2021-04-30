---
UID: NS:dhcpsapi._DHCP_FILTER_ADD_INFOV4
title: DHCP_FILTER_ADD_INFO (dhcpsapi.h)
description: Contains information regarding the link-layer filter to be added to the allow and deny filter list.
helpviewer_keywords: ["*LPDHCP_FILTER_ADD_INFO","DHCP_FILTER_ADD_INFO","DHCP_FILTER_ADD_INFO structure [DHCP]","PDHCP_FILTER_ADD_INFO","PDHCP_FILTER_ADD_INFO structure pointer [DHCP]","dhcp.dhcp_filter_add_info","dhcpsapi/DHCP_FILTER_ADD_INFO","dhcpsapi/PDHCP_FILTER_ADD_INFO"]
old-location: dhcp\dhcp_filter_add_info.htm
tech.root: DHCP
ms.assetid: eed7fffa-a48c-4ebc-ba3a-a118d2b0e20b
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_FILTER_ADD_INFO, DHCP_FILTER_ADD_INFO, DHCP_FILTER_ADD_INFO structure [DHCP], PDHCP_FILTER_ADD_INFO, PDHCP_FILTER_ADD_INFO structure pointer [DHCP], dhcp.dhcp_filter_add_info, dhcpsapi/DHCP_FILTER_ADD_INFO, dhcpsapi/PDHCP_FILTER_ADD_INFO'
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
req.typenames: DHCP_FILTER_ADD_INFO, *LPDHCP_FILTER_ADD_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_FILTER_ADD_INFOV4
 - dhcpsapi/_DHCP_FILTER_ADD_INFOV4
 - LPDHCP_FILTER_ADD_INFO
 - dhcpsapi/LPDHCP_FILTER_ADD_INFO
 - DHCP_FILTER_ADD_INFO
 - dhcpsapi/DHCP_FILTER_ADD_INFO
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
 - DHCP_FILTER_ADD_INFO
---

# DHCP_FILTER_ADD_INFO structure


## -description

The <b>DHCP_FILTER_ADD_INFO</b> structure contains information regarding the link-layer filter to be added to the allow and deny filter list.

## -struct-fields

### -field AddrPatt

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_addr_pattern">DHCP_ADDR_PATTERN</a> structure that contains the address/pattern-related information of the link-layer filter.

### -field Comment

Pointer to a Unicode string that contains a text comment for the filter.

### -field ListType

<a href="/windows/desktop/api/dhcpsapi/ne-dhcpsapi-dhcp_filter_list_type">DHCP_FILTER_LIST_TYPE</a> enumeration value that specifies the list type to which the filter is to be added.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_addr_pattern">DHCP_ADDR_PATTERN</a>



<a href="/windows/desktop/api/dhcpsapi/ne-dhcpsapi-dhcp_filter_list_type">DHCP_FILTER_LIST_TYPE</a>