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

# _DHCP_SUBNET_INFO_VQ structure


## -description


The <b>DHCP_SUBNET_INFO_VQ</b> structure defines information that describes a subnet.


## -struct-fields




### -field SubnetAddress


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> value that specifies the subnet ID.


### -field SubnetMask


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_MASK</a> value that specifies the subnet IP mask.


### -field SubnetName

Pointer to a Unicode string that specifies the network name of the subnet.


### -field SubnetComment

Pointer to a Unicode string that contains an optional comment particular to this subnet.


### -field PrimaryHost


<a href="https://msdn.microsoft.com/3d38f69d-2808-4e52-a3da-b6142578c981">DHCP_HOST_INFO</a> structure that contains information about the DHCP server servicing this subnet.


### -field SubnetState


<a href="https://msdn.microsoft.com/1f2960ae-98f2-4c93-9705-e8b74a4f5e21">DHCP_SUBNET_STATE</a> enumeration value indicating the current state of the subnet (enabled/disabled).


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

