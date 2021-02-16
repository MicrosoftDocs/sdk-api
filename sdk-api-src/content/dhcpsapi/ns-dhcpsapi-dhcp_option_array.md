---
UID: NS:dhcpsapi._DHCP_OPTION_ARRAY
title: DHCP_OPTION_ARRAY (dhcpsapi.h)
description: The DHCP_OPTION_ARRAY structure defines an array of DHCP server options.
helpviewer_keywords: ["*LPDHCP_OPTION_ARRAY","DHCP_OPTION_ARRAY","DHCP_OPTION_ARRAY structure [DHCP]","LPDHCP_OPTION_ARRAY","LPDHCP_OPTION_ARRAY structure pointer [DHCP]","dhcp.dhcp_option_array","dhcpsapi/DHCP_OPTION_ARRAY","dhcpsapi/LPDHCP_OPTION_ARRAY"]
old-location: dhcp\dhcp_option_array.htm
tech.root: DHCP
ms.assetid: 15b9bab5-8211-47c8-bc93-96c922c1aec1
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_OPTION_ARRAY, DHCP_OPTION_ARRAY, DHCP_OPTION_ARRAY structure [DHCP], LPDHCP_OPTION_ARRAY, LPDHCP_OPTION_ARRAY structure pointer [DHCP], dhcp.dhcp_option_array, dhcpsapi/DHCP_OPTION_ARRAY, dhcpsapi/LPDHCP_OPTION_ARRAY'
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.typenames: DHCP_OPTION_ARRAY, *LPDHCP_OPTION_ARRAY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_OPTION_ARRAY
 - dhcpsapi/_DHCP_OPTION_ARRAY
 - LPDHCP_OPTION_ARRAY
 - dhcpsapi/LPDHCP_OPTION_ARRAY
 - DHCP_OPTION_ARRAY
 - dhcpsapi/DHCP_OPTION_ARRAY
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
 - DHCP_OPTION_ARRAY
---

# DHCP_OPTION_ARRAY structure


## -description

The <b>DHCP_OPTION_ARRAY</b> structure defines an array of DHCP server options.

## -struct-fields

### -field NumElements

Specifies the number of option elements in <b>Options</b>.

### -field Options

Pointer to a list of <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option">DHCP_OPTION</a> structures containing DHCP server options and the associated data.

### -field Options.size_is

### -field Options.size_is.NumElements

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option">DHCP_OPTION</a>



<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_scope_info">DHCP_OPTION_SCOPE_INFO</a>