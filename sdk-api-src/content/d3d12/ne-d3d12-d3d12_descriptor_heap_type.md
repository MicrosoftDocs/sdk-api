---
UID: NE:d3d12.D3D12_DESCRIPTOR_HEAP_TYPE
title: D3D12_DESCRIPTOR_HEAP_TYPE (d3d12.h)
description: Specifies a type of descriptor heap.
helpviewer_keywords: ["D3D12_DESCRIPTOR_HEAP_TYPE","D3D12_DESCRIPTOR_HEAP_TYPE enumeration","D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV","D3D12_DESCRIPTOR_HEAP_TYPE_DSV","D3D12_DESCRIPTOR_HEAP_TYPE_NUM_TYPES","D3D12_DESCRIPTOR_HEAP_TYPE_RTV","D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER","d3d12/D3D12_DESCRIPTOR_HEAP_TYPE","d3d12/D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV","d3d12/D3D12_DESCRIPTOR_HEAP_TYPE_DSV","d3d12/D3D12_DESCRIPTOR_HEAP_TYPE_NUM_TYPES","d3d12/D3D12_DESCRIPTOR_HEAP_TYPE_RTV","d3d12/D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER","direct3d12.d3d12_descriptor_heap_type"]
old-location: direct3d12\d3d12_descriptor_heap_type.htm
tech.root: direct3d12
ms.assetid: E74C78BC-B0FC-473A-B4F3-434F50A55E9F
ms.date: 12/05/2018
ms.keywords: D3D12_DESCRIPTOR_HEAP_TYPE, D3D12_DESCRIPTOR_HEAP_TYPE enumeration, D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV, D3D12_DESCRIPTOR_HEAP_TYPE_DSV, D3D12_DESCRIPTOR_HEAP_TYPE_NUM_TYPES, D3D12_DESCRIPTOR_HEAP_TYPE_RTV, D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER, d3d12/D3D12_DESCRIPTOR_HEAP_TYPE, d3d12/D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV, d3d12/D3D12_DESCRIPTOR_HEAP_TYPE_DSV, d3d12/D3D12_DESCRIPTOR_HEAP_TYPE_NUM_TYPES, d3d12/D3D12_DESCRIPTOR_HEAP_TYPE_RTV, d3d12/D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER, direct3d12.d3d12_descriptor_heap_type
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
targetos: Windows
req.typenames: D3D12_DESCRIPTOR_HEAP_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_DESCRIPTOR_HEAP_TYPE
 - d3d12/D3D12_DESCRIPTOR_HEAP_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_DESCRIPTOR_HEAP_TYPE
---

# D3D12_DESCRIPTOR_HEAP_TYPE enumeration


## -description

Specifies a type of descriptor heap.

## -enum-fields

### -field D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV:0

The descriptor heap for the combination of constant-buffer, shader-resource, and unordered-access views.

### -field D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER

The descriptor heap for the sampler.

### -field D3D12_DESCRIPTOR_HEAP_TYPE_RTV

The descriptor heap for the render-target view.

### -field D3D12_DESCRIPTOR_HEAP_TYPE_DSV

The descriptor heap for the depth-stencil view.

### -field D3D12_DESCRIPTOR_HEAP_TYPE_NUM_TYPES

The number of types of descriptor heaps.

## -remarks

This enum is used by the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc">D3D12_DESCRIPTOR_HEAP_DESC</a> structure, and the following methods:

<ul>
<li>
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors">CopyDescriptors</a>
</li>
<li>
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple">CopyDescriptorsSimple</a>
</li>
<li>
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize">GetDescriptorHandleIncrementSize</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>



<a href="/windows/desktop/direct3d12/creating-descriptor-heaps">Creating Descriptor Heaps</a>



<a href="/windows/desktop/direct3d12/descriptor-heaps">Descriptor Heaps</a>
