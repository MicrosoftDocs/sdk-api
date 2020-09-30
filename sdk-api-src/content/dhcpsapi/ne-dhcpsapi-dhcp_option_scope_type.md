---
UID: NE:dhcpsapi._DHCP_OPTION_SCOPE_TYPE
title: DHCP_OPTION_SCOPE_TYPE (dhcpsapi.h)
description: The DHCP_OPTION_SCOPE_TYPE enumeration defines the set of possible DHCP option scopes.
helpviewer_keywords: ["*LPDHCP_OPTION_SCOPE_TYPE","DHCP_OPTION_SCOPE_TYPE","DHCP_OPTION_SCOPE_TYPE enumeration [DHCP]","DhcpDefaultOptions","DhcpGlobalOptions","DhcpMScopeOptions","DhcpReservedOptions","DhcpSubnetOptions","LPDHCP_OPTION_SCOPE_TYPE","LPDHCP_OPTION_SCOPE_TYPE enumeration pointer [DHCP]","dhcp.dhcp_option_scope_type","dhcpsapi/DHCP_OPTION_SCOPE_TYPE","dhcpsapi/DhcpDefaultOptions","dhcpsapi/DhcpGlobalOptions","dhcpsapi/DhcpMScopeOptions","dhcpsapi/DhcpReservedOptions","dhcpsapi/DhcpSubnetOptions","dhcpsapi/LPDHCP_OPTION_SCOPE_TYPE"]
old-location: dhcp\dhcp_option_scope_type.htm
tech.root: DHCP
ms.assetid: 3e49bbe4-a8d2-4e1a-b66d-a7d4b45dd670
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_OPTION_SCOPE_TYPE, DHCP_OPTION_SCOPE_TYPE, DHCP_OPTION_SCOPE_TYPE enumeration [DHCP], DhcpDefaultOptions, DhcpGlobalOptions, DhcpMScopeOptions, DhcpReservedOptions, DhcpSubnetOptions, LPDHCP_OPTION_SCOPE_TYPE, LPDHCP_OPTION_SCOPE_TYPE enumeration pointer [DHCP], dhcp.dhcp_option_scope_type, dhcpsapi/DHCP_OPTION_SCOPE_TYPE, dhcpsapi/DhcpDefaultOptions, dhcpsapi/DhcpGlobalOptions, dhcpsapi/DhcpMScopeOptions, dhcpsapi/DhcpReservedOptions, dhcpsapi/DhcpSubnetOptions, dhcpsapi/LPDHCP_OPTION_SCOPE_TYPE'
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
req.typenames: DHCP_OPTION_SCOPE_TYPE, *LPDHCP_OPTION_SCOPE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_OPTION_SCOPE_TYPE
 - dhcpsapi/_DHCP_OPTION_SCOPE_TYPE
 - LPDHCP_OPTION_SCOPE_TYPE
 - dhcpsapi/LPDHCP_OPTION_SCOPE_TYPE
 - DHCP_OPTION_SCOPE_TYPE
 - dhcpsapi/DHCP_OPTION_SCOPE_TYPE
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
 - DHCP_OPTION_SCOPE_TYPE
---

# DHCP_OPTION_SCOPE_TYPE enumeration


## -description

The <b>DHCP_OPTION_SCOPE_TYPE</b> enumeration defines the set of possible DHCP option scopes.

## -enum-fields

### -field DhcpDefaultOptions

The DHCP options correspond to the default scope.

### -field DhcpGlobalOptions

The  DHCP options correspond to the global scope.

### -field DhcpSubnetOptions

The  DHCP options correspond to a specific subnet scope.

### -field DhcpReservedOptions

The DHCP options correspond to a reserved IP address.

### -field DhcpMScopeOptions

The DHCP options correspond to a multicast scope.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_scope_info">DHCP_OPTION_SCOPE_INFO</a>