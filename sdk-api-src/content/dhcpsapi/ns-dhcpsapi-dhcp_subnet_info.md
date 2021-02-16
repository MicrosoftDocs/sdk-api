---
UID: NS:dhcpsapi._DHCP_SUBNET_INFO
title: DHCP_SUBNET_INFO (dhcpsapi.h)
description: The DHCP_SUBNET_INFO structure defines information describing a subnet.
helpviewer_keywords: ["*LPDHCP_SUBNET_INFO","DHCP_SUBNET_INFO","DHCP_SUBNET_INFO structure [DHCP]","LPDHCP_SUBNET_INFO","LPDHCP_SUBNET_INFO structure pointer [DHCP]","dhcp.dhcp_subnet_info","dhcpsapi/LPDHCP_SUBNET_INFO","dhcpsapi/_DHCP_SUBNET_INFO"]
old-location: dhcp\dhcp_subnet_info.htm
tech.root: DHCP
ms.assetid: 030b4743-7558-493c-931c-1ad28a6b435a
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_SUBNET_INFO, DHCP_SUBNET_INFO, DHCP_SUBNET_INFO structure [DHCP], LPDHCP_SUBNET_INFO, LPDHCP_SUBNET_INFO structure pointer [DHCP], dhcp.dhcp_subnet_info, dhcpsapi/LPDHCP_SUBNET_INFO, dhcpsapi/_DHCP_SUBNET_INFO'
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
req.typenames: DHCP_SUBNET_INFO, *LPDHCP_SUBNET_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_SUBNET_INFO
 - dhcpsapi/_DHCP_SUBNET_INFO
 - LPDHCP_SUBNET_INFO
 - dhcpsapi/LPDHCP_SUBNET_INFO
 - DHCP_SUBNET_INFO
 - dhcpsapi/DHCP_SUBNET_INFO
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
 - DHCP_SUBNET_INFO
---

# DHCP_SUBNET_INFO structure


## -description

The <b>DHCP_SUBNET_INFO</b> structure defines information describing a subnet.

## -struct-fields

### -field SubnetAddress

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> value that specifies the subnet ID.

### -field SubnetMask

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_MASK</a> value that specifies the subnet IP mask.

### -field SubnetName

Unicode string that specifies the network name of the subnet.

### -field SubnetComment

Unicode string that contains an optional comment particular to this subnet.

### -field PrimaryHost

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_host_info">DHCP_HOST_INFO</a> structure that contains information about the DHCP server servicing this subnet.

### -field SubnetState

<a href="/windows/desktop/api/dhcpsapi/ne-dhcpsapi-dhcp_subnet_state">DHCP_SUBNET_STATE</a> enumeration value indicating the current state of the subnet (enabled/disabled).

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_host_info">DHCP_HOST_INFO</a>



<a href="/windows/desktop/api/dhcpsapi/ne-dhcpsapi-dhcp_subnet_state">DHCP_SUBNET_STATE</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpgetsubnetinfo">DhcpGetSubnetInfo</a>