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

# _DHCP_SUPER_SCOPE_TABLE_ENTRY structure


## -description


The <b>DHCP_SUPER_SCOPE_TABLE_ENTRY</b> structure defines a subnet entry within the superscope table.


## -struct-fields




### -field SubnetAddress


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> value that specifies the IP address of the gateway for the subnet. This address is used to uniquely identify a subnet served by the DHCP server.


### -field SuperScopeNumber

Specifies the index value assigned to this subnet entry, and its enumerated position within the super scope table.


### -field NextInSuperScope

Specifies the index value of the next subnet entry in the superscope table. If this value is ---, this table entry is the last one in the super scope.


### -field SuperScopeName

Unicode string that contains the name assigned to this subnet entry within the superscope.


## -see-also




<a href="https://msdn.microsoft.com/ed7ad090-b13a-464b-af03-04944f018b36">DHCP_SUPER_SCOPE_TABLE</a>
 

 

