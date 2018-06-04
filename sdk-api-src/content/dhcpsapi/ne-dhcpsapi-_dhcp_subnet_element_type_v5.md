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

# _DHCP_SUBNET_ELEMENT_TYPE_V5 enumeration


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




<a href="https://msdn.microsoft.com/ea6df1bc-2d15-4a09-8100-ee17d3de34d9">DHCP_SUBNET_ELEMENT_DATA_V5</a>
 

 

