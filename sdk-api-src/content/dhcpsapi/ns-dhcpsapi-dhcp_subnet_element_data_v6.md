---
UID: NS:dhcpsapi._DHCP_SUBNET_ELEMENT_DATA_V6
title: DHCP_SUBNET_ELEMENT_DATA_V6 (dhcpsapi.h)
description: Contains definitions for the elements of the IPv6 prefix, such as IPv6 reservation, IPv6 exclusion range, and IPv6 range.
helpviewer_keywords: ["*LPDHCP_SUBNET_ELEMENT_DATA_V6","DHCP_SUBNET_ELEMENT_DATA_V6","DHCP_SUBNET_ELEMENT_DATA_V6 structure [DHCP]","PDHCP_SUBNET_ELEMENT_DATA_V6","PDHCP_SUBNET_ELEMENT_DATA_V6 structure pointer [DHCP]","dhcp.dhcp_subnet_element_data_v6","dhcpsapi/DHCP_SUBNET_ELEMENT_DATA_V6","dhcpsapi/PDHCP_SUBNET_ELEMENT_DATA_V6"]
old-location: dhcp\dhcp_subnet_element_data_v6.htm
tech.root: DHCP
ms.assetid: de5fa8c5-5cd7-4358-bacd-f27f4b7f3761
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_SUBNET_ELEMENT_DATA_V6, DHCP_SUBNET_ELEMENT_DATA_V6, DHCP_SUBNET_ELEMENT_DATA_V6 structure [DHCP], PDHCP_SUBNET_ELEMENT_DATA_V6, PDHCP_SUBNET_ELEMENT_DATA_V6 structure pointer [DHCP], dhcp.dhcp_subnet_element_data_v6, dhcpsapi/DHCP_SUBNET_ELEMENT_DATA_V6, dhcpsapi/PDHCP_SUBNET_ELEMENT_DATA_V6'
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
req.typenames: DHCP_SUBNET_ELEMENT_DATA_V6, *LPDHCP_SUBNET_ELEMENT_DATA_V6
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_SUBNET_ELEMENT_DATA_V6
 - dhcpsapi/_DHCP_SUBNET_ELEMENT_DATA_V6
 - LPDHCP_SUBNET_ELEMENT_DATA_V6
 - dhcpsapi/LPDHCP_SUBNET_ELEMENT_DATA_V6
 - DHCP_SUBNET_ELEMENT_DATA_V6
 - dhcpsapi/DHCP_SUBNET_ELEMENT_DATA_V6
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
 - DHCP_SUBNET_ELEMENT_DATA_V6
---

# DHCP_SUBNET_ELEMENT_DATA_V6 structure


## -description

The <b>DHCP_SUBNET_ELEMENT_DATA_V6</b> structure contains definitions for the elements of the IPv6 prefix, such as IPv6 reservation, IPv6 exclusion range, and IPv6 range.

## -struct-fields

### -field ElementType

Defines the set of possible prefix element types. This value is used to determine which of the values are chosen from the subsequent union element.

### -field Element.IpRange.case

### -field Element.IpRange.case.Dhcpv6IpRanges

### -field Element.ReservedIp.case

### -field Element.ReservedIp.case.Dhcpv6ReservedIps

### -field Element.ExcludeIpRange.case

### -field Element.ExcludeIpRange.case.Dhcpv6ExcludedIpRanges





### -field Element

A union of different IPv6 prefix element types. The value of this union is dependent on the <b>ElementType</b> member.

### -field Element.IpRange

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_ip_range_v6">DHCP_IP_RANGE_V6</a> structure that contains the IPv6 range for this IPv6 prefix.

### -field Element.ReservedIp

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_ip_reservation_v6">DHCP_IP_RESERVATION_V6</a> structure that contains the IPv6 reservation information.

### -field Element.ExcludeIpRange

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_ip_range_v6">DHCP_IP_RANGE_V6</a> structure that contains the IPv6 exclusion range information.

### -field _DHCP_SUBNET_ELEMENT_UNION_V6

## -see-also

<b>DHCP_IP_RANGE_V6</b>



<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_ip_reservation_v6">DHCP_IP_RESERVATION_V6</a>



<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_subnet_element_data_v6">DHCP_SUBNET_ELEMENT_DATA_V6</a>