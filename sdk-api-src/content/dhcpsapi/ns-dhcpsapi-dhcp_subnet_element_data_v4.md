---
UID: NS:dhcpsapi._DHCP_SUBNET_ELEMENT_DATA_V4
title: DHCP_SUBNET_ELEMENT_DATA_V4 (dhcpsapi.h)
author: windows-sdk-content
description: Defines an element that describes a feature or restriction of a subnet.
old-location: dhcp\dhcp_subnet_element_data_v4.htm
tech.root: DHCP
ms.assetid: d17725da-516b-4be6-839e-9876653e63c4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPDHCP_SUBNET_ELEMENT_DATA_V4, DHCP_SUBNET_ELEMENT_DATA_V4, DHCP_SUBNET_ELEMENT_DATA_V4 structure [DHCP], LPDHCP_SUBNET_ELEMENT_DATA_V4, LPDHCP_SUBNET_ELEMENT_DATA_V4 structure pointer [DHCP], dhcp.dhcp_subnet_element_data_v4, dhcpsapi/LPDHCP_SUBNET_ELEMENT_DATA_V4, dhcpsapi/_DHCP_SUBNET_ELEMENT_DATA_V4"
ms.topic: struct
f1_keywords: 
 - "dhcpsapi/DHCP_SUBNET_ELEMENT_DATA_V4"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dhcpsapi.h
api_name:
 - DHCP_SUBNET_ELEMENT_DATA_V4
product: Windows
targetos: Windows
req.typenames: DHCP_SUBNET_ELEMENT_DATA_V4, *LPDHCP_SUBNET_ELEMENT_DATA_V4
req.redist: 
ms.custom: 19H1
---

# DHCP_SUBNET_ELEMENT_DATA_V4 structure


## -description


The <b>DHCP_SUBNET_ELEMENT_DATA_V4</b> structure defines an element that describes a feature or restriction of a subnet. Together, a set of elements describes the set of IP addresses served for a subnet by DHCP. <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/ns-dhcpsapi-_dhcp_subnet_element_data_v5">DHCP_SUBNET_ELEMENT_DATA_V4</a> specifically allows for IP reservations that take client type into consideration

.


## -struct-fields




### -field ElementType


<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/ne-dhcpsapi-_dhcp_subnet_element_type_v5">DHCP_SUBNET_ELEMENT_TYPE</a> enumeration value describing the type of element in the subsequent field.


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

 


### -field Element.switch_is

 


### -field Element.switch_is.ELEMENT_MASK(ElementType)

 


### -field Element.switch_type

 


### -field Element.switch_type.DHCP_SUBNET_ELEMENT_TYPE

 


### -field Element


### -field Element.IpRange


<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/ns-dhcpsapi-_dhcp_ip_range">DHCP_IP_RANGE</a> structure that contains the set of DHCP-served IP addresses. This member is present if <b>ElementType</b> is set to <b>DhcpIpRanges</b>.


### -field Element.SecondaryHost


<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/ns-dhcpsapi-_dhcp_host_info">DHCP_HOST_INFO</a> structure that contains the IP addresses of secondary DHCP servers available on the subnet. This member is present if <b>ElementType</b> is set to <b>DhcpSecondaryHosts</b>.


### -field Element.ReservedIp


<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/ns-dhcpsapi-_dhcp_ip_reservation_v4">DHCP_IP_RESERVATION_V4</a> structure that contains the set of reserved IP addresses for the subnet. This member is present if <b>ElementType</b> is set to <b>DhcpExcludedIpRanges</b>.


### -field Element.ExcludeIpRange


<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/ns-dhcpsapi-_dhcp_ip_range">DHCP_IP_RANGE</a> structure that contains the set of excluded IP addresses. This member is present if <b>ElementType</b> is set to <b>DhcpExcludedIpRanges</b>.


### -field Element.IpUsedCluster


<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/ns-dhcpsapi-_dhcp_ip_cluster">DHCP_IP_CLUSTER</a> structure that contains the set of clusters within the subnet. This member is present if <b>ElementType</b> is set to <b>DhcpIpUsedClusters</b>.


### -field _DHCP_SUBNET_ELEMENT_UNION_V4

 




## -see-also




<a href="https://docs.microsoft.com/windows/win32/api/dhcpsapi/ns-dhcpsapi-dhcp_subnet_element_info_array_v4">DHCP_SUBNET_ELEMENT_INFO_ARRAY_V4</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/ne-dhcpsapi-_dhcp_subnet_element_type_v5">DHCP_SUBNET_ELEMENT_TYPE</a>
 

 

