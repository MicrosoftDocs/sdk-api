---
UID: NS:dhcpsapi._DHCP_OPTION
title: DHCP_OPTION (dhcpsapi.h)
description: The DHCP_OPTION structure defines a single DHCP option and any data elements associated with it.
helpviewer_keywords: ["*LPDHCP_OPTION","DHCP_OPTION","DHCP_OPTION structure [DHCP]","LPDHCP_OPTION","LPDHCP_OPTION structure pointer [DHCP]","dhcp.dhcp_option","dhcpsapi/DHCP_OPTION","dhcpsapi/LPDHCP_OPTION"]
old-location: dhcp\dhcp_option.htm
tech.root: DHCP
ms.assetid: 1be34eb4-a226-4f07-b763-173a4f8a0671
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_OPTION, DHCP_OPTION, DHCP_OPTION structure [DHCP], LPDHCP_OPTION, LPDHCP_OPTION structure pointer [DHCP], dhcp.dhcp_option, dhcpsapi/DHCP_OPTION, dhcpsapi/LPDHCP_OPTION'
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
req.typenames: DHCP_OPTION, *LPDHCP_OPTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_OPTION
 - dhcpsapi/_DHCP_OPTION
 - LPDHCP_OPTION
 - dhcpsapi/LPDHCP_OPTION
 - DHCP_OPTION
 - dhcpsapi/DHCP_OPTION
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
 - DHCP_OPTION
---

# DHCP_OPTION structure


## -description

The <b>DHCP_OPTION</b> structure defines a single DHCP option and any data elements associated with it.

## -struct-fields

### -field OptionID

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_OPTION_ID</a> value that specifies a unique ID number (also called a "code") for this option.

### -field OptionName

Unicode string that contains the name of this option.

### -field OptionComment

Unicode string that contains a comment about this option.

### -field DefaultValue

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_data">DHCP_OPTION_DATA</a> structure that contains the data associated with this option.

### -field OptionType

<a href="/windows/desktop/api/dhcpsapi/ne-dhcpsapi-dhcp_option_type">DHCP_OPTION_TYPE</a> enumeration value that indicates whether this option is a single unary item or an element in an array of options.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_array">DHCP_OPTION_ARRAY</a>



<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_data">DHCP_OPTION_DATA</a>



<a href="/windows/desktop/api/dhcpsapi/ne-dhcpsapi-dhcp_option_type">DHCP_OPTION_TYPE</a>