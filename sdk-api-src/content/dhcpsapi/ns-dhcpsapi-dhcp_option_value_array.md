---
UID: NS:dhcpsapi._DHCP_OPTION_VALUE_ARRAY
title: DHCP_OPTION_VALUE_ARRAY (dhcpsapi.h)
description: The DHCP_OPTION_VALUE_ARRAY structure defines a list of DHCP option values (just the option data with associated ID tags).
helpviewer_keywords: ["*LPDHCP_OPTION_VALUE_ARRAY","DHCP_OPTION_VALUE_ARRAY","DHCP_OPTION_VALUE_ARRAY structure [DHCP]","LPDHCP_OPTION_VALUE_ARRAY","LPDHCP_OPTION_VALUE_ARRAY structure pointer [DHCP]","dhcp.dhcp_option_value_array","dhcpsapi/LPDHCP_OPTION_VALUE_ARRAY","dhcpsapi/_DHCP_OPTION_VALUE_ARRAY"]
old-location: dhcp\dhcp_option_value_array.htm
tech.root: DHCP
ms.assetid: c68b9543-0d7a-46ab-babd-3868c1338d67
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_OPTION_VALUE_ARRAY, DHCP_OPTION_VALUE_ARRAY, DHCP_OPTION_VALUE_ARRAY structure [DHCP], LPDHCP_OPTION_VALUE_ARRAY, LPDHCP_OPTION_VALUE_ARRAY structure pointer [DHCP], dhcp.dhcp_option_value_array, dhcpsapi/LPDHCP_OPTION_VALUE_ARRAY, dhcpsapi/_DHCP_OPTION_VALUE_ARRAY'
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: DHCP_OPTION_VALUE_ARRAY, *LPDHCP_OPTION_VALUE_ARRAY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_OPTION_VALUE_ARRAY
 - dhcpsapi/_DHCP_OPTION_VALUE_ARRAY
 - LPDHCP_OPTION_VALUE_ARRAY
 - dhcpsapi/LPDHCP_OPTION_VALUE_ARRAY
 - DHCP_OPTION_VALUE_ARRAY
 - dhcpsapi/DHCP_OPTION_VALUE_ARRAY
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
 - DHCP_OPTION_VALUE_ARRAY
---

# DHCP_OPTION_VALUE_ARRAY structure


## -description

The <b>DHCP_OPTION_VALUE_ARRAY</b> structure defines a list of DHCP  option values (just the option data  with associated ID tags).

## -struct-fields

### -field NumElements

Specifies the number of option values listed in <b>Values</b>.

### -field Values

Pointer to a list of <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_value">DHCP_OPTION_VALUE</a> structures containing DHCP  option values.

### -field Values.size_is

### -field Values.size_is.NumElements