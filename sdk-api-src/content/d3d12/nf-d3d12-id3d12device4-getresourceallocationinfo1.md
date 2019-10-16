---
UID: NF:d3d12.ID3D12Device4.GetResourceAllocationInfo1
title: ID3D12Device4::GetResourceAllocationInfo1
author: windows-sdk-content
description: Gets rich info about the size and alignment of memory required for a collection of resources on this adapter.
tech.root: direct3d12
ms.author: windowssdkdev
ms.date: 10/15/2019
ms.keywords: ID3D12Device4 interface,GetResourceAllocationInfo1 method, ID3D12Device4.GetResourceAllocationInfo1, ID3D12Device4::GetResourceAllocationInfo1, GetResourceAllocationInfo1, GetResourceAllocationInfo1 method, GetResourceAllocationInfo1 method,ID3D12Device4 interface, direct3d12.id3d12device4_getresourceallocationinfo1, d3d12/ID3D12Device4::GetResourceAllocationInfo1
ms.topic: method
f1_keywords: 
 - "d3d12/ID3D12Device4.GetResourceAllocationInfo1"
dev_langs:
 - c++
req.construct-type: function
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
req.lib: d3d12.lib
req.dll: d3d12.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.lib
 - d3d12.dll
api_name:
 - ID3D12Device4::GetResourceAllocationInfo1
targetos: Windows
req.typenames: 
req.redist: 
---

## -description

Gets rich info about the size and alignment of memory required for a collection of resources on this adapter. Also see [ID3D12Device::GetResourceAllocationInfo](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo).

In addition to the [D3D12_RESOURCE_ALLOCATION_INFO](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) returned from the method, this version also returns an array of [D3D12_RESOURCE_ALLOCATION_INFO1](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_allocation_info1) structures, which provide additional details for each resource description passed as input. See the *pResourceAllocationInfo1* parameter.

## -parameters

### -param visibleMask [in]

Type: **[UINT](/windows/win32/WinProg/windows-data-types)**

For single-GPU operation, set this to zero. If there are multiple GPU nodes, then set bits to identify the nodes (the device's physical adapters). Each bit in the mask corresponds to a single node. Also see [Multi-adapter systems](/windows/win32/direct3d12/multi-engine).

### -param numResourceDescs [in]

Type: **[UINT](/windows/win32/WinProg/windows-data-types)**

The number of resource descriptors in the *pResourceDescs* array. This is also the size (the number of elements in) *pResourceAllocationInfo1*.

### -param pResourceDescs [in]

Type: **const [D3D12_RESOURCE_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc)\***

An array of **D3D12_RESOURCE_DESC** structures that described the resources to get info about.

### -param pResourceAllocationInfo1 [out]

Type: **[D3D12_RESOURCE_ALLOCATION_INFO1](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_allocation_info1)\***

An array of [D3D12_RESOURCE_ALLOCATION_INFO1](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_allocation_info1) structures, containing additional details for each resource description passed as input. This makes it simpler for your application to allocate a heap for multiple resources, and without manually computing offsets for where each resource should be placed.

## -returns

Type: **[D3D12_RESOURCE_ALLOCATION_INFO](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)**

A [D3D12_RESOURCE_ALLOCATION_INFO](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) structure that provides info about video memory allocated for the specified array of resources.

## -remarks

When you're using [CreatePlacedResource](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource), your application must use **GetResourceAllocationInfo** in order to understand the size and alignment characteristics of texture resources. The results of this method vary depending on the particular adapter, and must be treated as unique to this adapter and driver version.

Your application can't use the output of **GetResourceAllocationInfo** to understand packed mip properties of textures. To understand packed mip properties of textures, your application must use [GetResourceTiling](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourcetiling).

Texture resource sizes significantly differ from the information returned by **GetResourceTiling**, because some adapter architectures allocate extra memory for textures to reduce the effective bandwidth during common rendering scenarios. This even includes textures that have constraints on their texture layouts, or have standardized texture layouts. That extra memory can't be sparsely mapped nor remapped by an application using [CreateReservedResource](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createreservedresource) and [UpdateTileMappings](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings), so it isn't reported by **GetResourceTiling**.

Your application can forgo using **GetResourceAllocationInfo** for buffer resources ([D3D12_RESOURCE_DIMENSION_BUFFER](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension)). Buffers have the same size on all adapters, which is merely the smallest multiple of 64KB that's greater or equal to [D3D12_RESOURCE_DESC::Width](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc).

When multiple resource descriptions are passed in, the C++ algorithm for calculating a structure size and alignment are used. For example, a three-element array with two tiny 64KB-aligned resources and a tiny 4MB-aligned resource, reports differing sizes based on the order of the array. If the 4MB aligned resource is in the middle, then the resulting **Size** is 12MB. Otherwise, the resulting **Size** is 8MB. The **Alignment** returned would always be 4MB, because it's the superset of all alignments in the resource array.

## -see-also

[ID3D12Device4](/windows/win32/api/d3d12/nn-d3d12-id3d12device4)