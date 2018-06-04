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

# CLUS_FLAGS enumeration


## -description


Identifies the resource or group as a 
     <a href="https://msdn.microsoft.com/46b71882-be37-4c3f-a328-a394c1310958">core resource</a>.


## -enum-fields




### -field CLUS_FLAG_CORE

Identifies <a href="https://msdn.microsoft.com/46b71882-be37-4c3f-a328-a394c1310958">core resources</a> or the cluster group that 
       contains core resources. The 
       <a href="https://msdn.microsoft.com/a98ca55a-6535-48cf-a925-5005baa01b94">ClusterResourceControl</a> function with the 
       <a href="https://msdn.microsoft.com/bee0f0c4-4d8a-4903-a9d0-6b5bc1fdfce4">CLUSCTL_RESOURCE_GET_FLAGS</a> control 
       code can retrieve the flags that are set for a resource.


## -see-also




<a href="https://msdn.microsoft.com/bee0f0c4-4d8a-4903-a9d0-6b5bc1fdfce4">CLUSCTL_RESOURCE_GET_FLAGS</a>



<a href="https://msdn.microsoft.com/a98ca55a-6535-48cf-a925-5005baa01b94">ClusterResourceControl</a>
 

 

