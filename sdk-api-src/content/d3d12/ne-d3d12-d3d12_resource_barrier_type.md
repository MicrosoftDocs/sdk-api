---
UID: NE:d3d12.D3D12_RESOURCE_BARRIER_TYPE
title: D3D12_RESOURCE_BARRIER_TYPE
author: windows-sdk-content
description: Specifies a type of resource barrier (transition in resource use) description.
old-location: direct3d12\d3d12_resource_barrier_type.htm
old-project: direct3d12
ms.assetid: B3364C92-777F-4207-9685-534B2F07B48F
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: D3D12_RESOURCE_BARRIER_TYPE, D3D12_RESOURCE_BARRIER_TYPE enumeration, D3D12_RESOURCE_BARRIER_TYPE_ALIASING, D3D12_RESOURCE_BARRIER_TYPE_TRANSITION, D3D12_RESOURCE_BARRIER_TYPE_UAV, d3d12/D3D12_RESOURCE_BARRIER_TYPE, d3d12/D3D12_RESOURCE_BARRIER_TYPE_ALIASING, d3d12/D3D12_RESOURCE_BARRIER_TYPE_TRANSITION, d3d12/D3D12_RESOURCE_BARRIER_TYPE_UAV, direct3d12.d3d12_resource_barrier_type
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d3d12.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D3D12_RESOURCE_BARRIER_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_RESOURCE_BARRIER_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D12_RESOURCE_BARRIER_TYPE enumeration


## -description


Specifies a type of resource barrier (transition in resource use) description.


## -enum-fields




### -field D3D12_RESOURCE_BARRIER_TYPE_TRANSITION

A transition barrier that indicates a transition of a set of subresources between different usages. The caller must specify the before and after usages of the subresources. 


### -field D3D12_RESOURCE_BARRIER_TYPE_ALIASING

An aliasing barrier that indicates a transition between usages of 2 different resources that have mappings into the same tile pool. The caller can specify both the before and the after resource. Note that one or both resources can be <b>NULL</b>, which indicates that any tiled resource could cause aliasing.


### -field D3D12_RESOURCE_BARRIER_TYPE_UAV

An unordered access view (UAV) barrier that indicates all UAV accesses (reads or writes) to a particular resource must complete before any future UAV accesses (read or write) can begin. 


## -remarks



This enum is used in the <b>D3D12_RESOURCE_BARRIER_TYPE</b> structure. Use these values with the <a href="https://msdn.microsoft.com/AA788F94-122B-4132-BED5-162EAC683676">ID3D12GraphicsCommandList::ResourceBarrier</a> method.




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

