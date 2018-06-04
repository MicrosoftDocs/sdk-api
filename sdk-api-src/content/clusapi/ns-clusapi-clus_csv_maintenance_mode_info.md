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

# CLUS_CSV_MAINTENANCE_MODE_INFO structure


## -description


Used with the 
    <a href="https://msdn.microsoft.com/12c35048-660d-47d3-b35c-24eea5627ffb">CLUSCTL_RESOURCE_SET_CSV_MAINTENANCE_MODE</a> 
    control code to enables or disables the  maintenance mode on a cluster shared volume (CSV).


## -struct-fields




### -field InMaintenance

Specifies the maintenance mode for the CSV. <b>TRUE</b> enables maintenance mode, 
      <b>FALSE</b> disables it.


### -field VolumeName

The volume <b>GUID</b> path of the CSV.


## -see-also




<a href="https://msdn.microsoft.com/12c35048-660d-47d3-b35c-24eea5627ffb">CLUSCTL_RESOURCE_SET_CSV_MAINTENANCE_MODE</a>



<a href="https://msdn.microsoft.com/45da8dbc-dd70-4f95-b933-66d8e4340448">Utility structures</a>
 

 

