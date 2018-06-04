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

# _RESOURCE_EXIT_STATE enumeration


## -description


Enumerates the possible exit states of a 
    <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a>. These values are returned by the 
    <a href="https://msdn.microsoft.com/8ddb4578-f8c4-462e-af04-8c537d585e8b">SetResourceStatus</a> callback function.


## -enum-fields




### -field ResourceExitStateContinue

The resource has not been terminated. Worker threads may continue 
       <a href="https://msdn.microsoft.com/library/windows/hardware/dn997353">Online</a> and 
       <a href="https://msdn.microsoft.com/library/windows/hardware/dn997350">Offline</a> operations for the resource.


### -field ResourceExitStateTerminate

The resource has been terminated. Callers should end 
       <a href="https://msdn.microsoft.com/library/windows/hardware/dn997353">Online</a> or 
       <a href="https://msdn.microsoft.com/library/windows/hardware/dn997350">Offline</a> operations and immediately terminate all worker 
       threads assigned to the resource.


### -field ResourceExitStateMax

This value is only used for comparisons. All supported values are less than 
      <b>ResourceExitStateMax</b>.


## -see-also




<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>



<a href="https://msdn.microsoft.com/8ddb4578-f8c4-462e-af04-8c537d585e8b">SetResourceStatus</a>
 

 

