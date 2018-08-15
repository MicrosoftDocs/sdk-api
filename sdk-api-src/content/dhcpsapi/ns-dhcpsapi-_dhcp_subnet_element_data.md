---
UID: NS:dhcpsapi._DHCP_SUBNET_ELEMENT_DATA
title: "_DHCP_SUBNET_ELEMENT_DATA"
author: windows-sdk-content
description: Defines an element that describes a feature or restriction of a subnet.
old-location: dhcp\dhcp_subnet_element_data.htm
old-project: dhcp
ms.assetid: d6c32be0-a080-42c1-b9bf-3f5da2c4dbe0
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPDHCP_SUBNET_ELEMENT_DATA, DHCP_SUBNET_ELEMENT_DATA, DHCP_SUBNET_ELEMENT_DATA structure [DHCP], LPDHCP_SUBNET_ELEMENT_DATA, LPDHCP_SUBNET_ELEMENT_DATA structure pointer [DHCP], _DHCP_SUBNET_ELEMENT_DATA, dhcp.dhcp_subnet_element_data, dhcpsapi/LPDHCP_SUBNET_ELEMENT_DATA, dhcpsapi/_DHCP_SUBNET_ELEMENT_DATA"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dhcpsapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: DHCP_SUBNET_ELEMENT_DATA, *LPDHCP_SUBNET_ELEMENT_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dhcpsapi.h
api_name:
 - DHCP_SUBNET_ELEMENT_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DHCP_SUBNET_ELEMENT_DATA structure


## -description


The <b>DHCP_SUBNET_ELEMENT_DATA</b> structure defines an element that describes a feature or restriction of a subnet. Together, a set of elements describes the set of IP addresses served for a subnet by DHCP.


## -struct-fields




### -field ElementType


<a href="https://msdn.microsoft.com/291be329-0588-4b67-835f-4f2b2369772a">DHCP_SUBNET_ELEMENT_TYPE</a> enumeration value describing the type of element in the subsequent field.


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


<a href="https://msdn.microsoft.com/8d3f021d-25ac-44de-9bbc-cc558bc47f91">DHCP_IP_RANGE</a> structure that contains the set of DHCP-served IP addresses. This member is present if <b>ElementType</b> is set to <b>DhcpIpRanges</b>.


### -field Element.SecondaryHost


<a href="https://msdn.microsoft.com/3d38f69d-2808-4e52-a3da-b6142578c981">DHCP_HOST_INFO</a> structure that contains the IP addresses of secondary DHCP servers available on the subnet. This member is present if <b>ElementType</b> is set to <b>DhcpSecondaryHosts</b>.


### -field Element.ReservedIp


<a href="https://msdn.microsoft.com/35d7ebc7-790b-4453-a9d4-b485f0adac46">DHCP_IP_RESERVATION</a> structure that contains the set of reserved IP addresses for the subnet. This member is present if <b>ElementType</b> is set to <b>DhcpExcludedIpRanges</b>.


### -field Element.ExcludeIpRange


<a href="https://msdn.microsoft.com/8d3f021d-25ac-44de-9bbc-cc558bc47f91">DHCP_IP_RANGE</a> structure that contains the set of excluded IP addresses. This member is present if <b>ElementType</b> is set to <b>DhcpExcludedIpRanges</b>.


### -field Element.IpUsedCluster


<a href="https://msdn.microsoft.com/6dad62c3-c56f-4526-ae5c-dbb74cb13c8f">DHCP_IP_CLUSTER</a> structure that contains the set of clusters within the subnet. This member is present if <b>ElementType</b> is set to <b>DhcpIpUsedClusters</b>.


### -field _DHCP_SUBNET_ELEMENT_UNION

 




## -see-also




<a href="https://msdn.microsoft.com/50fbcae7-ea0c-4b46-a042-d463ab496e12">DHCP_SUBNET_ELEMENT_INFO_ARRAY</a>



<a href="https://msdn.microsoft.com/291be329-0588-4b67-835f-4f2b2369772a">DHCP_SUBNET_ELEMENT_TYPE</a>
 

 

