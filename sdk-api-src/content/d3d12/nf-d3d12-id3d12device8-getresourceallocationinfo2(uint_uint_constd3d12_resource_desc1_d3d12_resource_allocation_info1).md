---
UID: NF:d3d12.ID3D12Device8.GetResourceAllocationInfo2(UINT,UINT,constD3D12_RESOURCE_DESC1,D3D12_RESOURCE_ALLOCATION_INFO1)
title: ID3D12Device8::GetResourceAllocationInfo2
description: Gets rich info about the size and alignment of memory required for a collection of resources on this adapter. (ID3D12Device8::GetResourceAllocationInfo2)
helpviewer_keywords: ["ID3D12Device8 interface","GetResourceAllocationInfo2 method","ID3D12Device8.GetResourceAllocationInfo2","ID3D12Device8::GetResourceAllocationInfo2","GetResourceAllocationInfo2","GetResourceAllocationInfo2 method","GetResourceAllocationInfo2 method","ID3D12Device8 interface","direct3d12.id3d12device7_getresourceallocationinfo2","d3d12/ID3D12Device8::GetResourceAllocationInfo2"]
tech.root: direct3d12
ms.date: 09/16/2020
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: d3d12.dll
req.header: d3d12.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: d3d12.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12.lib
 - d3d12.dll
api_name:
 - ID3D12Device8::GetResourceAllocationInfo2
f1_keywords:
 - d3d12/ID3D12Device8::GetResourceAllocationInfo2
dev_langs:
 - c++
---

## -description

Gets rich info about the size and alignment of memory required for a collection of resources on this adapter. Also see [ID3D12Device4::GetResourceAllocationInfo1](./nf-d3d12-id3d12device4-getresourceallocationinfo1(uint_uint_constd3d12_resource_desc_d3d12_resource_allocation_info1).md).

This version also returns an array of [D3D12_RESOURCE_DESC1](./ns-d3d12-d3d12_resource_desc1.md) structures.

## -parameters

UINT numResourceDescs,
_In_reads_(numResourceDescs)  const D3D12_RESOURCE_DESC1 *pResourceDescs,
_Out_writes_opt_(numResourceDescs)  D3D12_RESOURCE_ALLOCATION_INFO1 *pResourceAllocationInfo1) = 0;

### -param visibleMask

Type: **[UINT](/windows/win32/WinProg/windows-data-types)**

For single-GPU operation, set this to zero. If there are multiple GPU nodes, then set bits to identify the nodes (the device's physical adapters). Each bit in the mask corresponds to a single node. Also see [Multi-adapter systems](/windows/win32/direct3d12/multi-engine).

### -param numResourceDescs

Type: **[UINT](/windows/win32/WinProg/windows-data-types)**

The number of resource descriptors in the *pResourceDescs* array. This is also the size (the number of elements in) *pResourceAllocationInfo1*.

### -param pResourceDescs

Type: **const [D3D12_RESOURCE_DESC1](./ns-d3d12-d3d12_resource_desc1.md)\***

An array of **D3D12_RESOURCE_DESC1** structures that described the resources to get info about.

### -param pResourceAllocationInfo1

Type: **[D3D12_RESOURCE_ALLOCATION_INFO1](./ns-d3d12-d3d12_resource_allocation_info1.md)\***

An array of [D3D12_RESOURCE_ALLOCATION_INFO1](./ns-d3d12-d3d12_resource_allocation_info1.md) structures, containing additional details for each resource description passed as input. This makes it simpler for your application to allocate a heap for multiple resources, and without manually computing offsets for where each resource should be placed.

## -returns

Type: **[D3D12_RESOURCE_ALLOCATION_INFO](./ns-d3d12-d3d12_resource_allocation_info.md)**

A [D3D12_RESOURCE_ALLOCATION_INFO](./ns-d3d12-d3d12_resource_allocation_info.md) structure that provides info about video memory allocated for the specified array of resources.

## -remarks

For remarks, see [ID3D12Device4::GetResourceAllocationInfo1](./nf-d3d12-id3d12device4-getresourceallocationinfo1(uint_uint_constd3d12_resource_desc_d3d12_resource_allocation_info1).md).

## -see-also

* [ID3D12Device8](./nn-d3d12-id3d12device8.md)

* [Sampler feedback specification](https://microsoft.github.io/DirectX-Specs/d3d/SamplerFeedback.html)
