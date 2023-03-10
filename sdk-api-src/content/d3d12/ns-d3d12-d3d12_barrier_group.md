---
UID: NS:d3d12.D3D12_BARRIER_GROUP
title: D3D12_BARRIER_GROUP
description: Describes a group of barriers of a given type.
tech.root: direct3d12
ms.date: 11/01/2022
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: d3d12.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: D3D12_BARRIER_GROUP
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - D3D12_BARRIER_GROUP
 - d3d12/D3D12_BARRIER_GROUP
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_BARRIER_GROUP
prerelease: false
---

## -description

Describes a group of barriers of a given type.

## -struct-fields

### -field Type

The type of barriers in the group.

### -field NumBarriers

The number of barriers in the group.

### -field pGlobalBarriers

A pointer to an array of [D3D12_GLOBAL_BARRIER](ns-d3d12-d3d12_global_barrier.md) structures, if *Type* is **D3D12_BARRIER_TYPE::D3D12_BARRIER_TYPE_GLOBAL**.

### -field pTextureBarriers

A pointer to an array of [D3D12_TEXTURE_BARRIER](ns-d3d12-d3d12_texture_barrier.md) structures, if *Type* is **D3D12_BARRIER_TYPE::D3D12_BARRIER_TYPE_TEXTURE**.

### -field pBufferBarriers

A pointer to an array of [D3D12_BUFFER_BARRIER](ns-d3d12-d3d12_buffer_barrier.md) structures, if *Type* is **D3D12_BARRIER_TYPE::D3D12_BARRIER_TYPE_BUFFER**.

## -remarks

## -see-also
