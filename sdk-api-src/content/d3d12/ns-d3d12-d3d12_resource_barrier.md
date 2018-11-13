---
UID: NS:d3d12.D3D12_RESOURCE_BARRIER
title: D3D12_RESOURCE_BARRIER
author: windows-sdk-content
description: Describes a resource barrier (transition in resource use).
old-location: direct3d12\d3d12_resource_barrier.htm
tech.root: direct3d12
ms.assetid: 49F02D65-767E-4BA4-A90D-68AA2D709E09
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: D3D12_RESOURCE_BARRIER, D3D12_RESOURCE_BARRIER structure, d3d12/D3D12_RESOURCE_BARRIER, direct3d12.d3d12_resource_barrier
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
 - D3D12.h
api_name:
 - D3D12_RESOURCE_BARRIER
product: Windows
targetos: Windows
req.typenames: D3D12_RESOURCE_BARRIER
req.redist: 
---

# D3D12_RESOURCE_BARRIER structure


## -description


Describes a resource barrier (transition in resource use).
        


## -struct-fields




### -field Type

A <a href="https://msdn.microsoft.com/B3364C92-777F-4207-9685-534B2F07B48F">D3D12_RESOURCE_BARRIER_TYPE</a>-typed value that specifies the type of resource barrier. 
            This member determines which type to use in the union below.
          


### -field Flags

Specifies a <a href="https://msdn.microsoft.com/352DF566-2E30-49C6-9D1B-35F0AEEA3338">D3D12_RESOURCE_BARRIER_FLAGS</a> enumeration constant such as for "begin only" or "end only".
          


### -field Transition

A <a href="https://msdn.microsoft.com/52C21198-827A-4E75-ADB8-DCA0204A4469">D3D12_RESOURCE_TRANSITION_BARRIER</a> structure that describes the transition of subresources between different usages.  
              Members specify the before and after usages of the subresources.
            


### -field Aliasing

A 
              <a href="https://msdn.microsoft.com/9855D609-E863-4334-B6BA-B6777FDAB82B">D3D12_RESOURCE_ALIASING_BARRIER</a>structure that describes the transition between usages of two different resources that have mappings into the same heap.
            


### -field UAV

A 
              <a href="https://msdn.microsoft.com/683F645F-9A90-4648-99EF-2F7444254B41">D3D12_RESOURCE_UAV_BARRIER</a>structure that describes a resource in which all UAV accesses (reads or writes) must complete before any future UAV accesses (read or write) can begin.
            


## -remarks



This structure is used by the <a href="https://msdn.microsoft.com/en-us/library/Dn903898(v=VS.85).aspx">ID3D12GraphicsCommandList::ResourceBarrier</a> method.
      




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn770459(v=VS.85).aspx">Core Structures</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn899226(v=VS.85).aspx">Using Resource Barriers to Synchronize Resource States in Direct3D 12</a>
 

 

