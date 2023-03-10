---
UID: NS:dhcpsapi._DHCP_ALL_OPTIONS
title: DHCP_ALL_OPTIONS (dhcpsapi.h)
description: Defines the set of all options available on a DHCP server.
helpviewer_keywords: ["*LPDHCP_ALL_OPTIONS","DHCP_ALL_OPTIONS","DHCP_ALL_OPTIONS structure [DHCP]","LPDHCP_ALL_OPTIONS","LPDHCP_ALL_OPTIONS structure pointer [DHCP]","dhcp.dhcp_all_options","dhcpsapi/LPDHCP_ALL_OPTIONS","dhcpsapi/_DHCP_ALL_OPTIONS"]
old-location: dhcp\dhcp_all_options.htm
tech.root: DHCP
ms.assetid: b02e3582-c99b-4d5a-aaae-c2fefd7dfaf9
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_ALL_OPTIONS, DHCP_ALL_OPTIONS, DHCP_ALL_OPTIONS structure [DHCP], LPDHCP_ALL_OPTIONS, LPDHCP_ALL_OPTIONS structure pointer [DHCP], dhcp.dhcp_all_options, dhcpsapi/LPDHCP_ALL_OPTIONS, dhcpsapi/_DHCP_ALL_OPTIONS'
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
req.typenames: DHCP_ALL_OPTIONS, *LPDHCP_ALL_OPTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_ALL_OPTIONS
 - dhcpsapi/_DHCP_ALL_OPTIONS
 - LPDHCP_ALL_OPTIONS
 - dhcpsapi/LPDHCP_ALL_OPTIONS
 - DHCP_ALL_OPTIONS
 - dhcpsapi/DHCP_ALL_OPTIONS
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
 - DHCP_ALL_OPTIONS
---

## -description

The <b>DHCP_ALL_OPTIONS</b> structure defines the set of all options available on a DHCP server.

## -struct-fields

### -field Flags

Reserved. This value should be set to 0.

### -field NonVendorOptions

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_array">DHCP_OPTION_ARRAY</a> structure that contains the set of non-vendor options.

### -field NumVendorOptions

Specifies the number of vendor options listed in <b>VendorOptions</b>.

### -field Option

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option">DHCP_OPTION</a> structure that contains specific information describing the option.

### -field VendorName

Unicode string that contains the name of the vendor for the option.

### -field ClassName

Unicode string that contains the name of the DHCP class for the option.

### -field VendorOptions

Pointer to a list of structures that contain the following fields.
