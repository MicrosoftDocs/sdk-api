---
UID: NE:d3d12.D3D12_DESCRIPTOR_HEAP_FLAGS
title: D3D12_DESCRIPTOR_HEAP_FLAGS
author: windows-sdk-content
description: Specifies options for a heap.
old-location: direct3d12\d3d12_descriptor_heap_flags.htm
tech.root: direct3d12
ms.assetid: 727178D9-D26C-48AF-86B0-E2E171940A11
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: D3D12_DESCRIPTOR_HEAP_FLAGS, D3D12_DESCRIPTOR_HEAP_FLAGS enumeration, D3D12_DESCRIPTOR_HEAP_FLAG_NONE, D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE, d3d12/D3D12_DESCRIPTOR_HEAP_FLAGS, d3d12/D3D12_DESCRIPTOR_HEAP_FLAG_NONE, d3d12/D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE, direct3d12.d3d12_descriptor_heap_flags
ms.prod: windows
ms.technology: windows-sdk
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
 - D3D12.h
api_name:
 - D3D12_DESCRIPTOR_HEAP_FLAGS
product: Windows
targetos: Windows
req.typenames: D3D12_DESCRIPTOR_HEAP_FLAGS
req.redist: 
---

# D3D12_DESCRIPTOR_HEAP_FLAGS enumeration


## -description


Specifies options for a heap.


## -enum-fields




### -field D3D12_DESCRIPTOR_HEAP_FLAG_NONE

Indicates default usage of a heap.


### -field D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE

The flag D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE can optionally be set on a descriptor heap to indicate it is be bound on a command list for reference by shaders.  Descriptor heaps created <i>without</i> this flag allow applications the option to stage descriptors in CPU memory before copying them to a shader visible descriptor heap, as a convenience.  But it is also fine for applications to directly create descriptors into shader visible descriptor heaps with no requirement to stage anything on the CPU.

This flag only applies to CBV, SRV, UAV and samplers. It does not apply to other descriptor heap types since shaders do not directly reference the other types.  


## -remarks



This enum is used by the <a href="https://msdn.microsoft.com/060ED49E-12B2-4DAE-A9DC-5BAB96B8E8ED">D3D12_DESCRIPTOR_HEAP_DESC</a> structure.
      




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>



<a href="https://msdn.microsoft.com/58677023-692C-4BA4-90B7-D568F3DD3F73">Creating Descriptor Heaps</a>



<a href="https://msdn.microsoft.com/04D3FACF-21EC-45CA-AD9B-78FDCDDC7136">Descriptor Heaps</a>
 

 

