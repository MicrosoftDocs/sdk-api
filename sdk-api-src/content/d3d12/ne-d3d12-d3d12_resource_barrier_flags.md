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

# D3D12_RESOURCE_BARRIER_FLAGS enumeration


## -description



          Flags for setting split resource barriers.
        


## -enum-fields




### -field D3D12_RESOURCE_BARRIER_FLAG_NONE


            No flags.
          


### -field D3D12_RESOURCE_BARRIER_FLAG_BEGIN_ONLY


            This starts a barrier transition in a new state, putting a resource in a temporary no-access condition.
          


### -field D3D12_RESOURCE_BARRIER_FLAG_END_ONLY


            This barrier completes a transition, setting a new state and restoring active access to a resource.


## -remarks



Split barriers allow a single transition to be split into begin and end halves (refer to <a href="https://msdn.microsoft.com/93903F50-A6CA-41C2-863D-68D645586B4C">Synchronization and Multi-Engine</a>).


          This enum is used by the <i>Flags</i> member of the
          <a href="https://msdn.microsoft.com/49F02D65-767E-4BA4-A90D-68AA2D709E09">D3D12_RESOURCE_BARRIER</a>
          structure.
         




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>



<a href="https://msdn.microsoft.com/AA788F94-122B-4132-BED5-162EAC683676">ResourceBarrier</a>



<a href="https://msdn.microsoft.com/3AB3BF34-433C-400B-921A-55B23CCDA44F">Using Resource Barriers to Synchronize Resource States in Direct3D 12</a>
 

 

