---
UID: NE:d3d12.D3D12_DESCRIPTOR_HEAP_FLAGS
title: D3D12_DESCRIPTOR_HEAP_FLAGS (d3d12.h)
description: Specifies options for a heap.
helpviewer_keywords: ["D3D12_DESCRIPTOR_HEAP_FLAGS","D3D12_DESCRIPTOR_HEAP_FLAGS enumeration","D3D12_DESCRIPTOR_HEAP_FLAG_NONE","D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE","d3d12/D3D12_DESCRIPTOR_HEAP_FLAGS","d3d12/D3D12_DESCRIPTOR_HEAP_FLAG_NONE","d3d12/D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE","direct3d12.d3d12_descriptor_heap_flags"]
old-location: direct3d12\d3d12_descriptor_heap_flags.htm
tech.root: direct3d12
ms.assetid: 727178D9-D26C-48AF-86B0-E2E171940A11
ms.date: 12/05/2018
ms.keywords: D3D12_DESCRIPTOR_HEAP_FLAGS, D3D12_DESCRIPTOR_HEAP_FLAGS enumeration, D3D12_DESCRIPTOR_HEAP_FLAG_NONE, D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE, d3d12/D3D12_DESCRIPTOR_HEAP_FLAGS, d3d12/D3D12_DESCRIPTOR_HEAP_FLAG_NONE, d3d12/D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE, direct3d12.d3d12_descriptor_heap_flags
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
req.typenames: D3D12_DESCRIPTOR_HEAP_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_DESCRIPTOR_HEAP_FLAGS
 - d3d12/D3D12_DESCRIPTOR_HEAP_FLAGS
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
 - D3D12_DESCRIPTOR_HEAP_FLAGS
---

## -description

Specifies options for a heap.

## -enum-fields

### -field D3D12_DESCRIPTOR_HEAP_FLAG_NONE:0

Indicates default usage of a heap.

### -field D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE:0x1

The flag [D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_heap_flags) can optionally be set on a descriptor heap to indicate it is be bound on a command list for reference by shaders. Descriptor heaps created <i>without</i> this flag allow applications the option to stage descriptors in CPU memory before copying them to a shader visible descriptor heap, as a convenience. But it is also fine for applications to directly create descriptors into shader visible descriptor heaps with no requirement to stage anything on the CPU.

Descriptor heaps bound via [ID3D12GraphicsCommandList::SetDescriptorHeaps](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps) must have the **D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE** flag set, else the debug layer will produce an error.

Descriptor heaps with the **D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE** flag can't be used as the source heaps in calls to [ID3D12Device::CopyDescriptors](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptors) or [ID3D12Device::CopyDescriptorsSimple](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple), because they could be resident in **WRITE_COMBINE** memory or GPU-local memory, which is very inefficient to read from.

This flag only applies to CBV/SRV/UAV descriptor heaps, and sampler descriptor heaps. It does not apply to other descriptor heap types since shaders do not directly reference the other types. Attempting to create an RTV/DSV heap with **D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE** results in a debug layer error.

## -remarks

This enum is used by the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc">D3D12_DESCRIPTOR_HEAP_DESC</a> structure.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>

<a href="/windows/desktop/direct3d12/creating-descriptor-heaps">Creating Descriptor Heaps</a>

<a href="/windows/desktop/direct3d12/descriptor-heaps">Descriptor Heaps</a>
