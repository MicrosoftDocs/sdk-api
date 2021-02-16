---
UID: NS:dhcpsapi._DHCP_SUBNET_ELEMENT_DATA_V5
title: DHCP_SUBNET_ELEMENT_DATA_V5 (dhcpsapi.h)
description: The DHCP_SUBNET_ELEMENT_DATA_V5 structure defines an element that describes a feature or restriction of a subnet.
helpviewer_keywords: ["*LPDHCP_SUBNET_ELEMENT_DATA_V5","DHCP_SUBNET_ELEMENT_DATA_V5","DHCP_SUBNET_ELEMENT_DATA_V5 structure [DHCP]","LPDHCP_SUBNET_ELEMENT_DATA_V5","LPDHCP_SUBNET_ELEMENT_DATA_V5 structure pointer [DHCP]","dhcp.dhcp_subnet_element_data_v5","dhcpsapi/LPDHCP_SUBNET_ELEMENT_DATA_V5","dhcpsapi/_DHCP_SUBNET_ELEMENT_DATA_V5"]
old-location: dhcp\dhcp_subnet_element_data_v5.htm
tech.root: DHCP
ms.assetid: ea6df1bc-2d15-4a09-8100-ee17d3de34d9
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_SUBNET_ELEMENT_DATA_V5, DHCP_SUBNET_ELEMENT_DATA_V5, DHCP_SUBNET_ELEMENT_DATA_V5 structure [DHCP], LPDHCP_SUBNET_ELEMENT_DATA_V5, LPDHCP_SUBNET_ELEMENT_DATA_V5 structure pointer [DHCP], dhcp.dhcp_subnet_element_data_v5, dhcpsapi/LPDHCP_SUBNET_ELEMENT_DATA_V5, dhcpsapi/_DHCP_SUBNET_ELEMENT_DATA_V5'
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
req.typenames: DHCP_SUBNET_ELEMENT_DATA_V5, *LPDHCP_SUBNET_ELEMENT_DATA_V5
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_SUBNET_ELEMENT_DATA_V5
 - dhcpsapi/_DHCP_SUBNET_ELEMENT_DATA_V5
 - LPDHCP_SUBNET_ELEMENT_DATA_V5
 - dhcpsapi/LPDHCP_SUBNET_ELEMENT_DATA_V5
 - DHCP_SUBNET_ELEMENT_DATA_V5
 - dhcpsapi/DHCP_SUBNET_ELEMENT_DATA_V5
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
 - DHCP_SUBNET_ELEMENT_DATA_V5
---

# DHCP_SUBNET_ELEMENT_DATA_V5 structure


## -description

The <b>DHCP_SUBNET_ELEMENT_DATA_V5</b> structure defines an element that describes a feature or restriction of a subnet. Together, a set of elements describes the set of IP addresses served for a subnet by DHCP or BOOTP. <b>DHCP_SUBNET_ELEMENT_DATA_V5</b> specifically allows for the definition of BOOTP-served addresses.

## -struct-fields

### -field ElementType

<a href="/windows/win32/api/dhcpsapi/ne-dhcpsapi-dhcp_subnet_element_type">DHCP_SUBNET_ELEMENT_TYPE</a> enumeration value describing the type of element in the subsequent field.

### -field Element.IpRange.case

### -field Element.IpRange.case.DhcpIpRanges

### -field Element.SecondaryHost.case

### -field Element.SecondaryHost.case.DhcpSecondaryHosts

### -field Element.ReservedIp.case

### -field Element.ReservedIp.case.DhcpReservedIps

### -field Element.ExcludeIpRange.case

### -field Element.ExcludeIpRange.case.DhcpExcludedIpRanges

### -field Element.IpUsedCluster.case

### -field Element.IpUsedCluster.case.DhcpIpUsedClusters



### -field Element.switch_type

### -field Element.switch_type.DHCP_SUBNET_ELEMENT_TYPE

### -field Element

### -field Element.IpRange

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_bootp_ip_range">DHCP_BOOTP_IP_RANGE</a> structure that contains the set of BOOTP-served IP addresses. This member is present if <b>ElementType</b> is set to <b>DhcpIpRangesBootpOnly</b>.

### -field Element.SecondaryHost

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_host_info">DHCP_HOST_INFO</a> structure that contains the IP addresses of secondary DHCP servers available on the subnet. This member is present if <b>ElementType</b> is set to <b>DhcpSecondaryHosts</b>.

### -field Element.ReservedIp

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_ip_reservation_v4">DHCP_IP_RESERVATION_V4</a> structure that contains the set of reserved IP addresses for the subnet. This member is present if <b>ElementType</b> is set to <b>DhcpReservedIps</b>.

### -field Element.ExcludeIpRange

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_ip_range">DHCP_IP_RANGE</a> structure that contains a range of IP addresses. This member is present if <b>ElementType</b> is set to <b>DhcpIpRanges</b> or <b>DhcpExcludedIpRanges</b>.

### -field Element.IpUsedCluster

### -field _DHCP_SUBNET_ELEMENT_UNION_V5