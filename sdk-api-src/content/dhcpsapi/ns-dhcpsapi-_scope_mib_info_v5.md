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

# _SCOPE_MIB_INFO_V5 structure


## -description


The <b>SCOPE_MIB_INFO_V5</b> structure contains information about a specific DHCP scope.


## -struct-fields




### -field Subnet


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> value that contains the IP address of the subnet gateway that defines the scope.


### -field NumAddressesInuse

 


### -field NumAddressesFree

The number of IP addresses in the scope that are not currently  assigned to DHCP clients.


### -field NumPendingOffers

The number of IP addresses in the scope that have been offered to DHCP clients but have not yet received REQUEST messages.


#### - NumAddressesInUse

The number of IP addresses in the scope that are currently assigned to DHCP clients.


## -see-also




<a href="https://msdn.microsoft.com/5081ebce-d3b9-4548-8d80-23d994bce7ab">DHCP_MIB_INFO_V5</a>



<a href="https://msdn.microsoft.com/3439198d-5391-4f9b-a6fe-9a600e7dc77b">DhcpGetMibInfoV5</a>
 

 

