---
UID: NE:dhcpsapi._DHCP_SUBNET_ELEMENT_TYPE_V5
title: DHCP_SUBNET_ELEMENT_TYPE (dhcpsapi.h)
description: The DHCP_SUBNET_ELEMENT_TYPE enumeration defines the set of possible subnet element types.
helpviewer_keywords: ["*LPDHCP_SUBNET_ELEMENT_TYPE","DHCP_SUBNET_ELEMENT_TYPE","DHCP_SUBNET_ELEMENT_TYPE enumeration [DHCP]","DhcpExcludedIpRanges","DhcpIpRanges","DhcpIpRangesBootpOnly","DhcpIpRangesDhcpBootp","DhcpIpRangesDhcpOnly","DhcpReservedIps","DhcpSecondaryHosts","LPDHCP_SUBNET_ELEMENT_TYPE","LPDHCP_SUBNET_ELEMENT_TYPE enumeration pointer [DHCP]","dhcp.dhcp_subnet_element_type","dhcpsapi/DHCP_SUBNET_ELEMENT_TYPE","dhcpsapi/DhcpExcludedIpRanges","dhcpsapi/DhcpIpRanges","dhcpsapi/DhcpIpRangesBootpOnly","dhcpsapi/DhcpIpRangesDhcpBootp","dhcpsapi/DhcpIpRangesDhcpOnly","dhcpsapi/DhcpReservedIps","dhcpsapi/DhcpSecondaryHosts","dhcpsapi/LPDHCP_SUBNET_ELEMENT_TYPE"]
old-location: dhcp\dhcp_subnet_element_type.htm
tech.root: DHCP
ms.assetid: 291be329-0588-4b67-835f-4f2b2369772a
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_SUBNET_ELEMENT_TYPE, DHCP_SUBNET_ELEMENT_TYPE, DHCP_SUBNET_ELEMENT_TYPE enumeration [DHCP], DhcpExcludedIpRanges, DhcpIpRanges, DhcpIpRangesBootpOnly, DhcpIpRangesDhcpBootp, DhcpIpRangesDhcpOnly, DhcpReservedIps, DhcpSecondaryHosts, LPDHCP_SUBNET_ELEMENT_TYPE, LPDHCP_SUBNET_ELEMENT_TYPE enumeration pointer [DHCP], dhcp.dhcp_subnet_element_type, dhcpsapi/DHCP_SUBNET_ELEMENT_TYPE, dhcpsapi/DhcpExcludedIpRanges, dhcpsapi/DhcpIpRanges, dhcpsapi/DhcpIpRangesBootpOnly, dhcpsapi/DhcpIpRangesDhcpBootp, dhcpsapi/DhcpIpRangesDhcpOnly, dhcpsapi/DhcpReservedIps, dhcpsapi/DhcpSecondaryHosts, dhcpsapi/LPDHCP_SUBNET_ELEMENT_TYPE'
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
req.typenames: DHCP_SUBNET_ELEMENT_TYPE, *LPDHCP_SUBNET_ELEMENT_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_SUBNET_ELEMENT_TYPE_V5
 - dhcpsapi/_DHCP_SUBNET_ELEMENT_TYPE_V5
 - LPDHCP_SUBNET_ELEMENT_TYPE
 - dhcpsapi/LPDHCP_SUBNET_ELEMENT_TYPE
 - DHCP_SUBNET_ELEMENT_TYPE
 - dhcpsapi/DHCP_SUBNET_ELEMENT_TYPE
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
 - DHCP_SUBNET_ELEMENT_TYPE
---

# DHCP_SUBNET_ELEMENT_TYPE enumeration


## -description

The <b>DHCP_SUBNET_ELEMENT_TYPE</b> enumeration defines the set of possible subnet element types.

## -enum-fields

### -field DhcpIpRanges

The subnet element contains the range of DHCP-served IP addresses.

### -field DhcpSecondaryHosts

The subnet element contains the IP addresses of secondary DHCP hosts available in the subnet.

### -field DhcpReservedIps

The subnet element contains the individual reserved IP addresses for the subnet.

### -field DhcpExcludedIpRanges

The subnet element contains the IP addresses excluded from the range of DHCP-served addresses.

### -field DhcpIpUsedClusters

### -field DhcpIpRangesDhcpOnly

The subnet element contains the IP addresses served by DHCP to the subnet (as opposed to those served by other dynamic address services, such as BOOTP).

### -field DhcpIpRangesDhcpBootp

The subnet element contains the IP addresses served by both DHCP and BOOTP to the subnet.

### -field DhcpIpRangesBootpOnly

The subnet element contains the IP addresses served by BOOTP to the subnet (specifically excluding DHCP-served addresses).

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_subnet_element_data_v5">DHCP_SUBNET_ELEMENT_DATA_V5</a>