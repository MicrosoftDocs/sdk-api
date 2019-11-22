---
UID: NS:dhcpsapi._DHCP_SUBNET_ELEMENT_DATA
title: DHCP_SUBNET_ELEMENT_DATA (dhcpsapi.h)

description: Defines an element that describes a feature or restriction of a subnet.
old-location: dhcp\dhcp_subnet_element_data.htm
tech.root: DHCP
ms.assetid: d6c32be0-a080-42c1-b9bf-3f5da2c4dbe0

ms.date: 12/05/2018
ms.keywords: '*LPDHCP_SUBNET_ELEMENT_DATA, DHCP_SUBNET_ELEMENT_DATA, DHCP_SUBNET_ELEMENT_DATA structure [DHCP], LPDHCP_SUBNET_ELEMENT_DATA, LPDHCP_SUBNET_ELEMENT_DATA structure pointer [DHCP], dhcp.dhcp_subnet_element_data, dhcpsapi/LPDHCP_SUBNET_ELEMENT_DATA, dhcpsapi/_DHCP_SUBNET_ELEMENT_DATA'
ms.topic: struct
f1_keywords:
- dhcpsapi/DHCP_SUBNET_ELEMENT_DATA
dev_langs:
 - c++
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
- DHCP_SUBNET_ELEMENT_DATA
targetos: Windows
req.typenames: DHCP_SUBNET_ELEMENT_DATA, *LPDHCP_SUBNET_ELEMENT_DATA
req.redist: 
ms.custom: 19H1
---

# DHCP_SUBNET_ELEMENT_DATA structure


## -description


The <b>DHCP_SUBNET_ELEMENT_DATA</b> structure defines an element that describes a feature or restriction of a subnet. Together, a set of elements describes the set of IP addresses served for a subnet by DHCP.


## -struct-fields




### -field ElementType


<a href="https://docs.microsoft.com/windows/win32/api/dhcpsapi/ne-dhcpsapi-dhcp_subnet_element_type">DHCP_SUBNET_ELEMENT_TYPE</a> enumeration value describing the type of element in the subsequent field.


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


<a href="https://docs.microsoft.com/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_ip_range">DHCP_IP_RANGE</a> structure that contains the set of DHCP-served IP addresses. This member is present if <b>ElementType</b> is set to <b>DhcpIpRanges</b>.


### -field Element.SecondaryHost


<a href="https://docs.microsoft.com/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_host_info">DHCP_HOST_INFO</a> structure that contains the IP addresses of secondary DHCP servers available on the subnet. This member is present if <b>ElementType</b> is set to <b>DhcpSecondaryHosts</b>.


### -field Element.ReservedIp


<a href="https://docs.microsoft.com/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_ip_reservation">DHCP_IP_RESERVATION</a> structure that contains the set of reserved IP addresses for the subnet. This member is present if <b>ElementType</b> is set to <b>DhcpExcludedIpRanges</b>.


### -field Element.ExcludeIpRange


<a href="https://docs.microsoft.com/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_ip_range">DHCP_IP_RANGE</a> structure that contains the set of excluded IP addresses. This member is present if <b>ElementType</b> is set to <b>DhcpExcludedIpRanges</b>.


### -field Element.IpUsedCluster


<a href="https://docs.microsoft.com/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_ip_cluster">DHCP_IP_CLUSTER</a> structure that contains the set of clusters within the subnet. This member is present if <b>ElementType</b> is set to <b>DhcpIpUsedClusters</b>.


### -field _DHCP_SUBNET_ELEMENT_UNION

 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_subnet_element_info_array">DHCP_SUBNET_ELEMENT_INFO_ARRAY</a>



<a href="https://docs.microsoft.com/windows/win32/api/dhcpsapi/ne-dhcpsapi-dhcp_subnet_element_type">DHCP_SUBNET_ELEMENT_TYPE</a>
 

 

