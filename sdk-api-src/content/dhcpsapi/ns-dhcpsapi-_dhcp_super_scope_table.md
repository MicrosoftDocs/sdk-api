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

# _DHCP_SUPER_SCOPE_TABLE structure


## -description


The <b>DHCP_SUPER_SCOPE_TABLE</b> structure defines the superscope of a DHCP server.


## -struct-fields




### -field cEntries

Specifies the number of subnets (and therefore scopes) present in the super scope.


### -field pEntries

Pointer to a list of <a href="https://msdn.microsoft.com/affaa0b0-3bd1-4d17-adec-518d2cb7e5b6">DHCP_SUPER_SCOPE_TABLE_ENTRY</a>
        structures containing the names and IP addresses of each subnet defined within the superscope.


### -field pEntries.size_is

 


### -field pEntries.size_is.cEntries

 




## -remarks



A "superscope" is the set of all subnets defined on a DHCP server, and hence all scopes along with the IP address ranges each serves. Taken altogether, it provides a complete set of all IP addresses served by the DHCP server. The superscope table will only provide the IP addresses associated with each subnet; to obtain the IP ranges served by each, <a href="https://msdn.microsoft.com/0e511993-a9c3-445b-bafc-3d66182ee32d">DhcpGetSubnetInfo</a> should be called on the IP address provided in each <a href="https://msdn.microsoft.com/affaa0b0-3bd1-4d17-adec-518d2cb7e5b6">DHCP_SUPER_SCOPE_TABLE_ENTRY</a>
        structure of the table.




## -see-also




<a href="https://msdn.microsoft.com/affaa0b0-3bd1-4d17-adec-518d2cb7e5b6">DHCP_SUPER_SCOPE_TABLE_ENTRY</a>



<a href="https://msdn.microsoft.com/f40c77b8-c8ad-432d-8a9e-6719630826ef">DhcpGetSuperScopeInfoV4</a>
 

 

