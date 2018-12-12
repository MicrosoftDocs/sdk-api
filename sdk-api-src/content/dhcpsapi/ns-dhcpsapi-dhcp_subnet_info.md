---
UID: NS:dhcpsapi._DHCP_SUBNET_INFO
title: DHCP_SUBNET_INFO
author: windows-sdk-content
description: The DHCP_SUBNET_INFO structure defines information describing a subnet.
old-location: dhcp\dhcp_subnet_info.htm
tech.root: DHCP
ms.assetid: 030b4743-7558-493c-931c-1ad28a6b435a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPDHCP_SUBNET_INFO, DHCP_SUBNET_INFO, DHCP_SUBNET_INFO structure [DHCP], LPDHCP_SUBNET_INFO, LPDHCP_SUBNET_INFO structure pointer [DHCP], dhcp.dhcp_subnet_info, dhcpsapi/LPDHCP_SUBNET_INFO, dhcpsapi/_DHCP_SUBNET_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dhcpsapi.h
api_name:
 - DHCP_SUBNET_INFO
product: Windows
targetos: Windows
req.typenames: DHCP_SUBNET_INFO, *LPDHCP_SUBNET_INFO
req.redist: 
---

# DHCP_SUBNET_INFO structure


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
 

 

