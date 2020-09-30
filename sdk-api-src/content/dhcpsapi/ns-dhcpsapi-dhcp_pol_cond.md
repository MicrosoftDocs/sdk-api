---
UID: NS:dhcpsapi._DHCP_POL_COND
title: DHCP_POL_COND (dhcpsapi.h)
description: The DHCP_POL_COND structure defines the DHCP server policy condition.
helpviewer_keywords: ["*LPDHCP_POL_COND","*PDHCP_POL_COND","DHCP_POL_COND","DHCP_POL_COND structure [DHCP]","LPDHCP_POL_COND","LPDHCP_POL_COND structure pointer [DHCP]","PDHCP_POL_COND","PDHCP_POL_COND structure pointer [DHCP]","dhcp.dhcp_pol_cond","dhcpsapi/DHCP_POL_COND","dhcpsapi/LPDHCP_POL_COND","dhcpsapi/PDHCP_POL_COND"]
old-location: dhcp\dhcp_pol_cond.htm
tech.root: DHCP
ms.assetid: 99A36029-1CBD-4A93-B25A-A0239D1C08D7
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_POL_COND, *PDHCP_POL_COND, DHCP_POL_COND, DHCP_POL_COND structure [DHCP], LPDHCP_POL_COND, LPDHCP_POL_COND structure pointer [DHCP], PDHCP_POL_COND, PDHCP_POL_COND structure pointer [DHCP], dhcp.dhcp_pol_cond, dhcpsapi/DHCP_POL_COND, dhcpsapi/LPDHCP_POL_COND, dhcpsapi/PDHCP_POL_COND'
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
req.typenames: DHCP_POL_COND, *PDHCP_POL_COND, *LPDHCP_POL_COND
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_POL_COND
 - dhcpsapi/_DHCP_POL_COND
 - PDHCP_POL_COND
 - dhcpsapi/PDHCP_POL_COND
 - DHCP_POL_COND
 - dhcpsapi/DHCP_POL_COND
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
 - DHCP_POL_COND
---

# DHCP_POL_COND structure


## -description

The <b>DHCP_POL_COND</b> structure defines the DHCP server policy condition.

## -struct-fields

### -field ParentExpr

Integer that specifies the expression index that corresponds to this constituent condition.

### -field Type

<a href="/previous-versions/windows/desktop/api/dhcpsapi/ne-dhcpsapi-dhcp_pol_attr_type">DHCP_POL_ATTR_TYPE</a> enumeration that specifies the attribute type for this condition.

### -field OptionID

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_OPTION_ID</a> value that specifies the unique option identifier for criteria based on DHCP options or sub-options.

### -field SubOptionID

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_OPTION_ID</a> value that specifies the unique sub-option identifier.

### -field VendorName

A pointer to a null-terminated Unicode string that represents the vendor name.

### -field Operator

<a href="/previous-versions/windows/desktop/api/dhcpsapi/ne-dhcpsapi-dhcp_pol_comparator">DHCP_POL_COMPARATOR</a> enumeration that specifies the comparison operator for the condition.

### -field Value

Pointer to an array of bytes that contains the value to be used for the comparison.

### -field Value.size_is

### -field Value.size_is.ValueLength

### -field ValueLength

Integer that specifies the length of <b>Value</b>.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_pol_cond_array">DHCP_POL_COND_ARRAY</a>