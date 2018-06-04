---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _DHCP_SUBNET_ELEMENT_DATA_V6 structure


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

 


### -field Element.switch_is

 


### -field Element.switch_is.ELEMENT_MASK(ElementType)

 


### -field Element.switch_type

 


### -field Element.switch_type.DHCP_SUBNET_ELEMENT_TYPE_V6

 


### -field Element

A union of different IPv6 prefix element types. The value of this union is dependent on the <b>ElementType</b> member.


### -field Element.IpRange

Pointer to a <a href="https://msdn.microsoft.com/3a918a2b-beff-4562-9c7f-acee2cc8f2da">DHCP_IP_RANGE_V6</a> structure that contains the IPv6 range for this IPv6 prefix.


### -field Element.ReservedIp

Pointer to a <a href="https://msdn.microsoft.com/f1595632-018b-4626-b3c6-49f0e5b3752c">DHCP_IP_RESERVATION_V6</a> structure that contains the IPv6 reservation information.


### -field Element.ExcludeIpRange

Pointer to a <a href="https://msdn.microsoft.com/3a918a2b-beff-4562-9c7f-acee2cc8f2da">DHCP_IP_RANGE_V6</a> structure that contains the IPv6 exclusion range information.


### -field _DHCP_SUBNET_ELEMENT_UNION_V6

 




## -see-also




<b>DHCP_IP_RANGE_V6</b>



<a href="https://msdn.microsoft.com/f1595632-018b-4626-b3c6-49f0e5b3752c">DHCP_IP_RESERVATION_V6</a>



<a href="https://msdn.microsoft.com/de5fa8c5-5cd7-4358-bacd-f27f4b7f3761">DHCP_SUBNET_ELEMENT_DATA_V6</a>
 

 

