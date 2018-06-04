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

# _DHCP_SUBNET_INFO structure


## -description


The <b>DHCP_SUBNET_INFO</b> structure defines information describing a subnet.


## -struct-fields




### -field SubnetAddress


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> value that specifies the subnet ID.


### -field SubnetMask


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_MASK</a> value that specifies the subnet IP mask.


### -field SubnetName

Unicode string that specifies the network name of the subnet.


### -field SubnetComment

Unicode string that contains an optional comment particular to this subnet.


### -field PrimaryHost


<a href="https://msdn.microsoft.com/3d38f69d-2808-4e52-a3da-b6142578c981">DHCP_HOST_INFO</a> structure that contains information about the DHCP server servicing this subnet.


### -field SubnetState


<a href="https://msdn.microsoft.com/1f2960ae-98f2-4c93-9705-e8b74a4f5e21">DHCP_SUBNET_STATE</a> enumeration value indicating the current state of the subnet (enabled/disabled).


## -see-also




<a href="https://msdn.microsoft.com/3d38f69d-2808-4e52-a3da-b6142578c981">DHCP_HOST_INFO</a>



<a href="https://msdn.microsoft.com/1f2960ae-98f2-4c93-9705-e8b74a4f5e21">DHCP_SUBNET_STATE</a>



<a href="https://msdn.microsoft.com/0e511993-a9c3-445b-bafc-3d66182ee32d">DhcpGetSubnetInfo</a>
 

 

