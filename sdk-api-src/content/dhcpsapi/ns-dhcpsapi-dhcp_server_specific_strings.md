---
UID: NS:dhcpsapi._DHCP_SERVER_SPECIFIC_STRINGS
title: DHCP_SERVER_SPECIFIC_STRINGS (dhcpsapi.h)
description: Contains the default string values for user and vendor class names.
helpviewer_keywords: ["*LPDHCP_SERVER_SPECIFIC_STRINGS","DHCP_SERVER_SPECIFIC_STRINGS","DHCP_SERVER_SPECIFIC_STRINGS structure [DHCP]","PDHCP_SERVER_SPECIFIC_STRINGS","PDHCP_SERVER_SPECIFIC_STRINGS structure pointer [DHCP]","dhcp.dhcp_server_specific_strings","dhcpsapi/DHCP_SERVER_SPECIFIC_STRINGS","dhcpsapi/PDHCP_SERVER_SPECIFIC_STRINGS"]
old-location: dhcp\dhcp_server_specific_strings.htm
tech.root: DHCP
ms.assetid: 5fc52d5c-22b0-454b-bc07-8f9c4ca163e3
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_SERVER_SPECIFIC_STRINGS, DHCP_SERVER_SPECIFIC_STRINGS, DHCP_SERVER_SPECIFIC_STRINGS structure [DHCP], PDHCP_SERVER_SPECIFIC_STRINGS, PDHCP_SERVER_SPECIFIC_STRINGS structure pointer [DHCP], dhcp.dhcp_server_specific_strings, dhcpsapi/DHCP_SERVER_SPECIFIC_STRINGS, dhcpsapi/PDHCP_SERVER_SPECIFIC_STRINGS'
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
req.typenames: DHCP_SERVER_SPECIFIC_STRINGS, *LPDHCP_SERVER_SPECIFIC_STRINGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_SERVER_SPECIFIC_STRINGS
 - dhcpsapi/_DHCP_SERVER_SPECIFIC_STRINGS
 - LPDHCP_SERVER_SPECIFIC_STRINGS
 - dhcpsapi/LPDHCP_SERVER_SPECIFIC_STRINGS
 - DHCP_SERVER_SPECIFIC_STRINGS
 - dhcpsapi/DHCP_SERVER_SPECIFIC_STRINGS
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
 - DHCP_SERVER_SPECIFIC_STRINGS
---

# DHCP_SERVER_SPECIFIC_STRINGS structure


## -description

The <b>DHCP_SERVER_SPECIFIC_STRINGS</b> structure contains the default string values for user and vendor class names.

## -struct-fields

### -field DefaultVendorClassName

Pointer to a Unicode string that specifies the default vendor class name for the DHCP server.

### -field DefaultUserClassName

Pointer to a Unicode string that specifies the default user class name for the DHCP server.

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpgetserverspecificstrings">DhcpGetServerSpecificStrings</a>