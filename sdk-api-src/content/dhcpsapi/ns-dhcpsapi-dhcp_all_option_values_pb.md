---
UID: NS:dhcpsapi._DHCP_ALL_OPTION_VALUES_PB
title: DHCP_ALL_OPTION_VALUES_PB (dhcpsapi.h)
description: The DHCP_ALL_OPTION_VALUES_PB structure defines the set of all option values for a DHCP server within a scope.
helpviewer_keywords: ["*LPDHCP_ALL_OPTION_VALUES_PB","DHCP_ALL_OPTION_VALUES_PB","DHCP_ALL_OPTION_VALUES_PB structure [DHCP]","LPDHCP_ALL_OPTION_VALUES_PB","LPDHCP_ALL_OPTION_VALUES_PB structure pointer [DHCP]","dhcp.dhcp_all_option_values_pb","dhcpsapi/DHCP_ALL_OPTION_VALUES_PB","dhcpsapi/LPDHCP_ALL_OPTION_VALUES_PB"]
old-location: dhcp\dhcp_all_option_values_pb.htm
tech.root: DHCP
ms.assetid: 5b43263a-fea1-452b-9981-a0f2cf1c8cf0
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_ALL_OPTION_VALUES_PB, DHCP_ALL_OPTION_VALUES_PB, DHCP_ALL_OPTION_VALUES_PB structure [DHCP], LPDHCP_ALL_OPTION_VALUES_PB, LPDHCP_ALL_OPTION_VALUES_PB structure pointer [DHCP], dhcp.dhcp_all_option_values_pb, dhcpsapi/DHCP_ALL_OPTION_VALUES_PB, dhcpsapi/LPDHCP_ALL_OPTION_VALUES_PB'
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
req.typenames: DHCP_ALL_OPTION_VALUES_PB, *LPDHCP_ALL_OPTION_VALUES_PB
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_ALL_OPTION_VALUES_PB
 - dhcpsapi/_DHCP_ALL_OPTION_VALUES_PB
 - LPDHCP_ALL_OPTION_VALUES_PB
 - dhcpsapi/LPDHCP_ALL_OPTION_VALUES_PB
 - DHCP_ALL_OPTION_VALUES_PB
 - dhcpsapi/DHCP_ALL_OPTION_VALUES_PB
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
 - DHCP_ALL_OPTION_VALUES_PB
---

# DHCP_ALL_OPTION_VALUES_PB structure


## -description

The <b>DHCP_ALL_OPTION_VALUES_PB</b> structure defines the set of all option values for a DHCP server within a scope.

## -struct-fields

### -field Flags

Reserved. Must be 0.

### -field NumElements

Integer that specifies the number of elements in <b>Options</b>.

### -field PolicyName

Pointer to a null-terminated Unicode string that represents the DHCP server policy name for the option set. <b>NULL</b> if none exists.

### -field VendorName

Pointer to a null-terminated Unicode string that represents the vendor name  for the option set. <b>NULL</b> if none exists.

### -field IsVendor

<b>TRUE</b> if the option set is vendor-specific. Otherwise, it is <b>FALSE</b>.

### -field OptionsArray

[DHCP_OPTION_VALUE_ARRAY](/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_value_array) structure that contains the option values for the specified vendor/class pair.

### -field Options

Pointer to a list of [DHCP_OPTION_VALUE_ARRAY](/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_value_array) structures that contain the set of all option values for specific vendor/policy pairs. There is one element per pair.

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4getalloptionvalues">DhcpV4GetAllOptionValues</a>
