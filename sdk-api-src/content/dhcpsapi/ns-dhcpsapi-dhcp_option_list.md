---
UID: NS:dhcpsapi._DHCP_OPTION_LIST
title: DHCP_OPTION_LIST (dhcpsapi.h)
description: Defines a list of DHCP option values (just the option data with associated ID tags).
helpviewer_keywords: ["*LPDHCP_OPTION_LIST","DHCP_OPTION_LIST","DHCP_OPTION_LIST structure [DHCP]","LPDHCP_OPTION_LIST","LPDHCP_OPTION_LIST structure pointer [DHCP]","dhcp.dhcp_option_list","dhcpsapi/LPDHCP_OPTION_LIST","dhcpsapi/_DHCP_OPTION_LIST"]
old-location: dhcp\dhcp_option_list.htm
tech.root: DHCP
ms.assetid: ffe9ed82-1aec-4e09-8258-399099c87b5a
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_OPTION_LIST, DHCP_OPTION_LIST, DHCP_OPTION_LIST structure [DHCP], LPDHCP_OPTION_LIST, LPDHCP_OPTION_LIST structure pointer [DHCP], dhcp.dhcp_option_list, dhcpsapi/LPDHCP_OPTION_LIST, dhcpsapi/_DHCP_OPTION_LIST'
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2008 R2 [desktop apps only]
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
req.typenames: DHCP_OPTION_LIST, *LPDHCP_OPTION_LIST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_OPTION_LIST
 - dhcpsapi/_DHCP_OPTION_LIST
 - LPDHCP_OPTION_LIST
 - dhcpsapi/LPDHCP_OPTION_LIST
 - DHCP_OPTION_LIST
 - dhcpsapi/DHCP_OPTION_LIST
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
 - DHCP_OPTION_LIST
---

# DHCP_OPTION_LIST structure


## -description

The <b>DHCP_OPTION_LIST</b> structure defines a list of DHCP option values (just the option data  with associated ID tags).

## -struct-fields

### -field NumOptions

Specifies the number of option values  listed in <b>Options</b>.

### -field Options

Pointer to a list of <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_value">DHCP_OPTION_VALUE</a> structures

### -field Options.size_is

### -field Options.size_is.NumOptions

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_value">DHCP_OPTION_VALUE</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpgetclientoptions">DhcpGetClientOptions</a>