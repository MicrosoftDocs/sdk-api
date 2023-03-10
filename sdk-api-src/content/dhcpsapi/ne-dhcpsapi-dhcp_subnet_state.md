---
UID: NE:dhcpsapi._DHCP_SUBNET_STATE
title: DHCP_SUBNET_STATE (dhcpsapi.h)
description: The DHCP_SUBNET_STATE enumeration defines the set of possible states for a subnet.
helpviewer_keywords: ["*LPDHCP_SUBNET_STATE","DHCP_SUBNET_STATE","DHCP_SUBNET_STATE enumeration [DHCP]","DhcpSubnetDisabled","DhcpSubnetDisabledSwitched","DhcpSubnetEnabled","DhcpSubnetEnabledSwitched","DhcpSubnetInvalidState","LPDHCP_SUBNET_STATE","LPDHCP_SUBNET_STATE enumeration pointer [DHCP]","dhcp.dhcp_subnet_state","dhcpsapi/DHCP_SUBNET_STATE","dhcpsapi/DhcpSubnetDisabled","dhcpsapi/DhcpSubnetDisabledSwitched","dhcpsapi/DhcpSubnetEnabled","dhcpsapi/DhcpSubnetEnabledSwitched","dhcpsapi/DhcpSubnetInvalidState","dhcpsapi/LPDHCP_SUBNET_STATE"]
old-location: dhcp\dhcp_subnet_state.htm
tech.root: DHCP
ms.assetid: 1f2960ae-98f2-4c93-9705-e8b74a4f5e21
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_SUBNET_STATE, DHCP_SUBNET_STATE, DHCP_SUBNET_STATE enumeration [DHCP], DhcpSubnetDisabled, DhcpSubnetDisabledSwitched, DhcpSubnetEnabled, DhcpSubnetEnabledSwitched, DhcpSubnetInvalidState, LPDHCP_SUBNET_STATE, LPDHCP_SUBNET_STATE enumeration pointer [DHCP], dhcp.dhcp_subnet_state, dhcpsapi/DHCP_SUBNET_STATE, dhcpsapi/DhcpSubnetDisabled, dhcpsapi/DhcpSubnetDisabledSwitched, dhcpsapi/DhcpSubnetEnabled, dhcpsapi/DhcpSubnetEnabledSwitched, dhcpsapi/DhcpSubnetInvalidState, dhcpsapi/LPDHCP_SUBNET_STATE'
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
req.typenames: DHCP_SUBNET_STATE, *LPDHCP_SUBNET_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_SUBNET_STATE
 - dhcpsapi/_DHCP_SUBNET_STATE
 - LPDHCP_SUBNET_STATE
 - dhcpsapi/LPDHCP_SUBNET_STATE
 - DHCP_SUBNET_STATE
 - dhcpsapi/DHCP_SUBNET_STATE
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
 - DHCP_SUBNET_STATE
---

# DHCP_SUBNET_STATE enumeration


## -description

The <b>DHCP_SUBNET_STATE</b> enumeration defines the set of possible states for a subnet.

## -enum-fields

### -field DhcpSubnetEnabled:0

The subnet is enabled; the server will distribute addresses, extend leases, and release addresses within the subnet range to clients.

### -field DhcpSubnetDisabled

The subnet is disabled; the server will not distribute addresses or extend leases within the subnet range to clients. However, the server will still release addresses within the subnet range.

### -field DhcpSubnetEnabledSwitched

The subnet is enabled; the server will distribute addresses, extend leases, and release addresses within the subnet range to clients. The default gateway is set to the local machine itself.

### -field DhcpSubnetDisabledSwitched

The subnet is disabled; the server will not distribute addresses or extend leases within the subnet range to clients. However, the server will still release addresses within the subnet range. The default gateway is set to the local machine itself.

### -field DhcpSubnetInvalidState

The subnet is in an invalid state.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_subnet_info">DHCP_SUBNET_INFO</a>
