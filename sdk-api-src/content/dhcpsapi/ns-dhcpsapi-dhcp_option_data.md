---
UID: NS:dhcpsapi._DHCP_OPTION_DATA
title: DHCP_OPTION_DATA (dhcpsapi.h)
description: The DHCP_OPTION_DATA structure defines a data container for one or more data elements associated with a DHCP option.
helpviewer_keywords: ["*LPDHCP_OPTION_DATA","DHCP_OPTION_DATA","DHCP_OPTION_DATA structure [DHCP]","LPDHCP_OPTION_DATA","LPDHCP_OPTION_DATA structure pointer [DHCP]","dhcp.dhcp_option_data","dhcpsapi/LPDHCP_OPTION_DATA","dhcpsapi/_DHCP_OPTION_DATA"]
old-location: dhcp\dhcp_option_data.htm
tech.root: DHCP
ms.assetid: 6b2e5866-f65f-4ff0-a531-3d07b972f55e
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_OPTION_DATA, DHCP_OPTION_DATA, DHCP_OPTION_DATA structure [DHCP], LPDHCP_OPTION_DATA, LPDHCP_OPTION_DATA structure pointer [DHCP], dhcp.dhcp_option_data, dhcpsapi/LPDHCP_OPTION_DATA, dhcpsapi/_DHCP_OPTION_DATA'
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
req.typenames: DHCP_OPTION_DATA, *LPDHCP_OPTION_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_OPTION_DATA
 - dhcpsapi/_DHCP_OPTION_DATA
 - LPDHCP_OPTION_DATA
 - dhcpsapi/LPDHCP_OPTION_DATA
 - DHCP_OPTION_DATA
 - dhcpsapi/DHCP_OPTION_DATA
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
 - DHCP_OPTION_DATA
---

# DHCP_OPTION_DATA structure


## -description

The <b>DHCP_OPTION_DATA</b> structure defines a data container for one or more data elements associated with a DHCP option.

## -struct-fields

### -field NumElements

Specifies the number of option data elements listed in <b>Elements</b>.

### -field Elements

Pointer to a list of <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_data_element">DHCP_OPTION_DATA_ELEMENT</a> structures that contain the data elements associated with this particular option element.

### -field Elements.size_is

### -field Elements.size_is.NumElements

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_data_element">DHCP_OPTION_DATA_ELEMENT</a>