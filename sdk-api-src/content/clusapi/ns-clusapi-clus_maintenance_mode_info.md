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

# CLUS_MAINTENANCE_MODE_INFO structure


## -description


Enables or disables maintenance mode on a cluster node.


## -struct-fields




### -field InMaintenance

Set to <b>TRUE</b> to enable or <b>FALSE</b> to disable maintenance 
      mode for the identified resource.

When queried, a resource will return <b>True</b> or <b>False</b> to 
       indicate the current maintenance mode state of the resource.


## -remarks



When using <a href="https://msdn.microsoft.com/a98ca55a-6535-48cf-a925-5005baa01b94">ClusterResourceControl</a> to enable 
    or disable maintenance mode on a specified resource, the calling routine can specify a larger buffer with addition 
    resource-specific data by including it immediately after the 
    <b>CLUS_MAINTENANCE_MODE_INFO</b> structure. This 
    data then becomes private to the resource as it cannot be retrieved by the calling program using the 
    <a href="https://msdn.microsoft.com/ceaaf124-bc66-4e5b-b5c3-2cae7f7c5a14">CLUSCTL_RESOURCE_QUERY_MAINTENANCE_MODE</a> 
    control code.




## -see-also




<a href="https://msdn.microsoft.com/ceaaf124-bc66-4e5b-b5c3-2cae7f7c5a14">CLUSCTL_RESOURCE_QUERY_MAINTENANCE_MODE</a>



<a href="https://msdn.microsoft.com/211de9d9-7fcb-47b7-a6b3-ee1bc241f176">CLUSCTL_RESOURCE_SET_MAINTENANCE_MODE</a>



<a href="https://msdn.microsoft.com/a98ca55a-6535-48cf-a925-5005baa01b94">ClusterResourceControl</a>



<a href="https://msdn.microsoft.com/45da8dbc-dd70-4f95-b933-66d8e4340448">Utility structures</a>
 

 

