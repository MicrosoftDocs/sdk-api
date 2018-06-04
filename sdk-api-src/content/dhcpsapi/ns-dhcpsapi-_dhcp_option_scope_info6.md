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

# _DHCP_OPTION_SCOPE_INFO6 structure


## -description


The DHCP_OPTION_SCOPE_INFO6 structure defines the data associated with a DHCP option scope.


## -struct-fields




### -field ScopeType


<a href="https://msdn.microsoft.com/dc6811ca-571e-4d63-ac30-8a9038cb28af">DHCP_OPTION_SCOPE_TYPE6</a> enumeration value that indicates the type of the DHCP option. This value is used as the selector for the union arms listed in the following fields.


### -field ScopeInfo.SubnetScopeInfo.case

 


### -field ScopeInfo.SubnetScopeInfo.case.DhcpScopeOptions6

 


### -field ScopeInfo.ReservedScopeInfo.case

 


### -field ScopeInfo.ReservedScopeInfo.case.DhcpReservedOptions6

 


### -field ScopeInfo.switch_is

 


### -field ScopeInfo.switch_is.ScopeType

 


### -field ScopeInfo.switch_type

 


### -field ScopeInfo.switch_type.DHCP_OPTION_SCOPE_TYPE6

 


### -field ScopeInfo


### -field ScopeInfo.DefaultScopeInfo

Pointer to data the specifies the default scope information. This must be set to null.


### -field ScopeInfo.SubnetScopeInfo

IPv6 mask for the subnet that defines the DHCP scope.


### -field ScopeInfo.ReservedScopeInfo

DHCP_RESERVED_SCOPE6 structure that contains the reserved DHCP scope information.


### -field _DHCP_OPTION_SCOPE_UNION6

 




## -see-also




<a href="https://msdn.microsoft.com/dc6811ca-571e-4d63-ac30-8a9038cb28af">DHCP_OPTION_SCOPE_TYPE6</a>
 

 

