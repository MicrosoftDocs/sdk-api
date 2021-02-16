---
UID: NS:dhcpsapi._DHCP_OPTION_VALUE
title: DHCP_OPTION_VALUE (dhcpsapi.h)
description: The DHCP_OPTION_VALUE structure defines a DHCP option value (just the option data with an associated ID tag).
helpviewer_keywords: ["*LPDHCP_OPTION_VALUE","DHCP_OPTION_VALUE","DHCP_OPTION_VALUE structure [DHCP]","LPDHCP_OPTION_VALUE","LPDHCP_OPTION_VALUE structure pointer [DHCP]","dhcp.dhcp_option_value","dhcpsapi/LPDHCP_OPTION_VALUE","dhcpsapi/_DHCP_OPTION_VALUE"]
old-location: dhcp\dhcp_option_value.htm
tech.root: DHCP
ms.assetid: 6a11cb60-2690-45d4-a5e6-a3ebdc1efe3d
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_OPTION_VALUE, DHCP_OPTION_VALUE, DHCP_OPTION_VALUE structure [DHCP], LPDHCP_OPTION_VALUE, LPDHCP_OPTION_VALUE structure pointer [DHCP], dhcp.dhcp_option_value, dhcpsapi/LPDHCP_OPTION_VALUE, dhcpsapi/_DHCP_OPTION_VALUE'
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
req.typenames: DHCP_OPTION_VALUE, *LPDHCP_OPTION_VALUE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_OPTION_VALUE
 - dhcpsapi/_DHCP_OPTION_VALUE
 - LPDHCP_OPTION_VALUE
 - dhcpsapi/LPDHCP_OPTION_VALUE
 - DHCP_OPTION_VALUE
 - dhcpsapi/DHCP_OPTION_VALUE
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
 - DHCP_OPTION_VALUE
---

# DHCP_OPTION_VALUE structure


## -description

The <b>DHCP_OPTION_VALUE</b> structure defines a DHCP  option value (just the option data with an associated ID tag).

## -struct-fields

### -field OptionID

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_OPTION_ID</a> value that specifies a unique ID number for the option.

### -field Value

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_data">DHCP_OPTION_DATA</a> structure that contains the data for a DHCP server option.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_data">DHCP_OPTION_DATA</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpgetoptionvalue">DhcpGetOptionValue</a>