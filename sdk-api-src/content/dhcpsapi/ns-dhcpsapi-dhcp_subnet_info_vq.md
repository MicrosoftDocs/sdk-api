---
UID: NS:dhcpsapi._DHCP_SUBNET_INFO_VQ
title: DHCP_SUBNET_INFO_VQ (dhcpsapi.h)
description: Defines information that describes a subnet.
helpviewer_keywords: ["*LPDHCP_SUBNET_INFO_VQ","DHCP_SUBNET_INFO_VQ","DHCP_SUBNET_INFO_VQ structure [DHCP]","LPDHCP_SUBNET_INFO_VQ","LPDHCP_SUBNET_INFO_VQ structure pointer [DHCP]","dhcp.dhcp_subnet_info_vq","dhcpsapi/DHCP_SUBNET_INFO_VQ","dhcpsapi/LPDHCP_SUBNET_INFO_VQ"]
old-location: dhcp\dhcp_subnet_info_vq.htm
tech.root: DHCP
ms.assetid: 8440378e-c1dc-4e22-8c56-2cf4412c2483
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_SUBNET_INFO_VQ, DHCP_SUBNET_INFO_VQ, DHCP_SUBNET_INFO_VQ structure [DHCP], LPDHCP_SUBNET_INFO_VQ, LPDHCP_SUBNET_INFO_VQ structure pointer [DHCP], dhcp.dhcp_subnet_info_vq, dhcpsapi/DHCP_SUBNET_INFO_VQ, dhcpsapi/LPDHCP_SUBNET_INFO_VQ'
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
req.typenames: DHCP_SUBNET_INFO_VQ, *LPDHCP_SUBNET_INFO_VQ
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_SUBNET_INFO_VQ
 - dhcpsapi/_DHCP_SUBNET_INFO_VQ
 - LPDHCP_SUBNET_INFO_VQ
 - dhcpsapi/LPDHCP_SUBNET_INFO_VQ
 - DHCP_SUBNET_INFO_VQ
 - dhcpsapi/DHCP_SUBNET_INFO_VQ
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
 - DHCP_SUBNET_INFO_VQ
---

# DHCP_SUBNET_INFO_VQ structure


## -description

The <b>DHCP_SUBNET_INFO_VQ</b> structure defines information that describes a subnet.

## -struct-fields

### -field SubnetAddress

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> value that specifies the subnet ID.

### -field SubnetMask

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_MASK</a> value that specifies the subnet IP mask.

### -field SubnetName

Pointer to a Unicode string that specifies the network name of the subnet.

### -field SubnetComment

Pointer to a Unicode string that contains an optional comment particular to this subnet.

### -field PrimaryHost

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_host_info">DHCP_HOST_INFO</a> structure that contains information about the DHCP server servicing this subnet.

### -field SubnetState

<a href="/windows/desktop/api/dhcpsapi/ne-dhcpsapi-dhcp_subnet_state">DHCP_SUBNET_STATE</a> enumeration value indicating the current state of the subnet (enabled/disabled).

### -field QuarantineOn

Integer value used as a BOOL to represent whether or not Quarantine is enabled for the subnet. If <b>TRUE</b> (0x00000001), Quarantine is turned ON on the DHCP server; if <b>FALSE</b> (0x00000000), it is turned OFF.

### -field Reserved1

Reserved for future use.

### -field Reserved2

Reserved for future use.

### -field Reserved3

Reserved for future use.

### -field Reserved4

Reserved for future use.