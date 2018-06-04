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

# _SCOPE_MIB_INFO structure


## -description


The <b>SCOPE_MIB_INFO</b> structure defines information about an available scope for use within returned DHCP-specific SNMP Management Information Block (MIB) data.


## -struct-fields




### -field Subnet


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> value that specifies the subnet mask for this scope.


### -field NumAddressesInuse

Contains the number of IP addresses currently in use for this scope.


### -field NumAddressesFree

Contains the number of IP addresses currently available for this scope.


### -field NumPendingOffers

Contains the number of IP addresses currently in the offer state for this scope.


## -see-also




<a href="https://msdn.microsoft.com/58f3e3a3-8246-48ff-be45-20a7eed1ed0e">DHCP_MIB_INFO</a>



<a href="https://msdn.microsoft.com/8b961666-4b55-47b4-be52-81b67c9d1cae">DHCP_MIB_INFO_V6</a>
 

 

