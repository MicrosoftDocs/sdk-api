---
UID: NS:dhcpsapi._DHCP_FILTER_RECORD
title: DHCP_FILTER_RECORD (dhcpsapi.h)
description: Contains information for a specific link-layer filter.
helpviewer_keywords: ["*LPDHCP_FILTER_RECORD","DHCP_FILTER_RECORD","DHCP_FILTER_RECORD structure [DHCP]","PDHCP_FILTER_RECORD","PDHCP_FILTER_RECORD structure pointer [DHCP]","dhcp.dhcp_filter_record","dhcpsapi/DHCP_FILTER_RECORD","dhcpsapi/PDHCP_FILTER_RECORD"]
old-location: dhcp\dhcp_filter_record.htm
tech.root: DHCP
ms.assetid: 5f8531fe-cc30-4baf-904b-15627d1ff750
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_FILTER_RECORD, DHCP_FILTER_RECORD, DHCP_FILTER_RECORD structure [DHCP], PDHCP_FILTER_RECORD, PDHCP_FILTER_RECORD structure pointer [DHCP], dhcp.dhcp_filter_record, dhcpsapi/DHCP_FILTER_RECORD, dhcpsapi/PDHCP_FILTER_RECORD'
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
req.typenames: DHCP_FILTER_RECORD, *LPDHCP_FILTER_RECORD
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_FILTER_RECORD
 - dhcpsapi/_DHCP_FILTER_RECORD
 - LPDHCP_FILTER_RECORD
 - dhcpsapi/LPDHCP_FILTER_RECORD
 - DHCP_FILTER_RECORD
 - dhcpsapi/DHCP_FILTER_RECORD
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
 - DHCP_FILTER_RECORD
---

# DHCP_FILTER_RECORD structure


## -description

The <b>DHCP_FILTER_RECORD</b> structure contains information for a specific link-layer filter.

## -struct-fields

### -field AddrPatt

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_addr_pattern">DHCP_ADDR_PATTERN</a> structure that contains the address/pattern related information of the link-layer filter.

### -field Comment

Pointer to a null-terminated Unicode string which contains the comment associated with the address/pattern.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_addr_pattern">DHCP_ADDR_PATTERN</a>