---
UID: NS:d3d12.D3D12_GPU_VIRTUAL_ADDRESS_AND_STRIDE
title: D3D12_GPU_VIRTUAL_ADDRESS_AND_STRIDE (d3d12.h)
description: Represents a GPU virtual address and indexing stride.
helpviewer_keywords: ["D3D12_GPU_VIRTUAL_ADDRESS_AND_STRIDE","D3D12_GPU_VIRTUAL_ADDRESS_AND_STRIDE structure","PD3D12_GPU_VIRTUAL_ADDRESS_AND_STRIDE","PD3D12_GPU_VIRTUAL_ADDRESS_AND_STRIDE structure pointer","d3d12/D3D12_GPU_VIRTUAL_ADDRESS_AND_STRIDE","d3d12/PD3D12_GPU_VIRTUAL_ADDRESS_AND_STRIDE","direct3d12.d3d12_gpu_virtual_address_and_stride"]
old-location: direct3d12\d3d12_gpu_virtual_address_and_stride.htm
tech.root: direct3d12
ms.assetid: 2A90A58A-24B6-45D7-9F79-FB80739EB823
ms.date: 12/05/2018
ms.keywords: D3D12_GPU_VIRTUAL_ADDRESS_AND_STRIDE, D3D12_GPU_VIRTUAL_ADDRESS_AND_STRIDE structure, PD3D12_GPU_VIRTUAL_ADDRESS_AND_STRIDE, PD3D12_GPU_VIRTUAL_ADDRESS_AND_STRIDE structure pointer, d3d12/D3D12_GPU_VIRTUAL_ADDRESS_AND_STRIDE, d3d12/PD3D12_GPU_VIRTUAL_ADDRESS_AND_STRIDE, direct3d12.d3d12_gpu_virtual_address_and_stride
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
req.typenames: D3D12_GPU_VIRTUAL_ADDRESS_AND_STRIDE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_GPU_VIRTUAL_ADDRESS_AND_STRIDE
 - d3d12/D3D12_GPU_VIRTUAL_ADDRESS_AND_STRIDE
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
 - D3D12_GPU_VIRTUAL_ADDRESS_AND_STRIDE
---

# D3D12_GPU_VIRTUAL_ADDRESS_AND_STRIDE structure


## -description

Represents a GPU virtual address and indexing stride.

## -struct-fields

### -field StartAddress

The beginning of the virtual address range.

### -field StrideInBytes

Defines indexing stride, such as for vertices.  Only the bottom 32 bits are used.  The field is 64 bits to make alignment of containing structures consistent everywhere.

