---
UID: NE:dhcpsapi._DHCP_OPTION_SCOPE_TYPE6
title: DHCP_OPTION_SCOPE_TYPE6 (dhcpsapi.h)
description: Defines the set of possible scopes for DHCP options.
helpviewer_keywords: ["*LPDHCP_OPTION_SCOPE_TYPE6","DHCP_OPTION_SCOPE_TYPE6","DHCP_OPTION_SCOPE_TYPE6 enumeration [DHCP]","DhcpDefaultOptions6","DhcpReservedOptions6","DhcpScopeOptions6","dhcp.dhcp_option_scope_type6","dhcpsapi/DHCP_OPTION_SCOPE_TYPE6","dhcpsapi/DhcpDefaultOptions6","dhcpsapi/DhcpReservedOptions6","dhcpsapi/DhcpScopeOptions6"]
old-location: dhcp\dhcp_option_scope_type6.htm
tech.root: DHCP
ms.assetid: dc6811ca-571e-4d63-ac30-8a9038cb28af
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_OPTION_SCOPE_TYPE6, DHCP_OPTION_SCOPE_TYPE6, DHCP_OPTION_SCOPE_TYPE6 enumeration [DHCP], DhcpDefaultOptions6, DhcpReservedOptions6, DhcpScopeOptions6, dhcp.dhcp_option_scope_type6, dhcpsapi/DHCP_OPTION_SCOPE_TYPE6, dhcpsapi/DhcpDefaultOptions6, dhcpsapi/DhcpReservedOptions6, dhcpsapi/DhcpScopeOptions6'
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
req.typenames: DHCP_OPTION_SCOPE_TYPE6, *LPDHCP_OPTION_SCOPE_TYPE6
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_OPTION_SCOPE_TYPE6
 - dhcpsapi/_DHCP_OPTION_SCOPE_TYPE6
 - LPDHCP_OPTION_SCOPE_TYPE6
 - dhcpsapi/LPDHCP_OPTION_SCOPE_TYPE6
 - DHCP_OPTION_SCOPE_TYPE6
 - dhcpsapi/DHCP_OPTION_SCOPE_TYPE6
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
 - DHCP_OPTION_SCOPE_TYPE6
---

# DHCP_OPTION_SCOPE_TYPE6 enumeration


## -description

The DHCP_OPTION_SCOPE_TYPE6 enumeration defines the set of possible scopes for DHCP options.

## -enum-fields

### -field DhcpDefaultOptions6

The default set of DHCP options are selected.

### -field DhcpScopeOptions6

Only DHCP options defined for this scope are selected.

### -field DhcpReservedOptions6

Only the reserved set of DHCP options are selected.

### -field DhcpGlobalOptions6

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_scope_info6">DHCP_OPTION_SCOPE_INFO6</a>