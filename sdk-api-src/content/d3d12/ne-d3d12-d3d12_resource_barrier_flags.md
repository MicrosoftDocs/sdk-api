---
UID: NE:d3d12.D3D12_RESOURCE_BARRIER_FLAGS
title: D3D12_RESOURCE_BARRIER_FLAGS
author: windows-sdk-content
description: Flags for setting split resource barriers.
old-location: direct3d12\d3d12_resource_barrier_flags.htm
tech.root: direct3d12
ms.assetid: 352DF566-2E30-49C6-9D1B-35F0AEEA3338
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D12_RESOURCE_BARRIER_FLAGS, D3D12_RESOURCE_BARRIER_FLAGS enumeration, D3D12_RESOURCE_BARRIER_FLAG_BEGIN_ONLY, D3D12_RESOURCE_BARRIER_FLAG_END_ONLY, D3D12_RESOURCE_BARRIER_FLAG_NONE, d3d12/D3D12_RESOURCE_BARRIER_FLAGS, d3d12/D3D12_RESOURCE_BARRIER_FLAG_BEGIN_ONLY, d3d12/D3D12_RESOURCE_BARRIER_FLAG_END_ONLY, d3d12/D3D12_RESOURCE_BARRIER_FLAG_NONE, direct3d12.d3d12_resource_barrier_flags
ms.topic: enum
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_RESOURCE_BARRIER_FLAGS
product: Windows
targetos: Windows
req.typenames: D3D12_RESOURCE_BARRIER_FLAGS
req.redist: 
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
          <a href="https://msdn.microsoft.com/49F02D65-767E-4BA4-A90D-68AA2D709E09">D3D12_RESOURCE_BARRIER</a>structure.
         




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>



<a href="https://msdn.microsoft.com/AA788F94-122B-4132-BED5-162EAC683676">ResourceBarrier</a>



<a href="https://msdn.microsoft.com/3AB3BF34-433C-400B-921A-55B23CCDA44F">Using Resource Barriers to Synchronize Resource States in Direct3D 12</a>
 

 

