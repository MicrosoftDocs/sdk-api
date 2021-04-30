---
UID: NS:d3d12.D3D12_MEMCPY_DEST
title: D3D12_MEMCPY_DEST (d3d12.h)
description: Describes the destination of a memory copy operation.
helpviewer_keywords: ["D3D12_MEMCPY_DEST","D3D12_MEMCPY_DEST structure","d3d12/D3D12_MEMCPY_DEST","direct3d12.d3d12_memcpy_dest"]
old-location: direct3d12\d3d12_memcpy_dest.htm
tech.root: direct3d12
ms.assetid: B85B7B60-FA34-4A4D-B1A7-D54884956E83
ms.date: 12/05/2018
ms.keywords: D3D12_MEMCPY_DEST, D3D12_MEMCPY_DEST structure, d3d12/D3D12_MEMCPY_DEST, direct3d12.d3d12_memcpy_dest
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
req.typenames: D3D12_MEMCPY_DEST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_MEMCPY_DEST
 - d3d12/D3D12_MEMCPY_DEST
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
 - D3D12_MEMCPY_DEST
---

# D3D12_MEMCPY_DEST structure


## -description

Describes the destination of a memory copy operation.

## -struct-fields

### -field pData

A pointer to a memory block that receives the copied data.

### -field RowPitch

The row pitch, or width, or physical size, in bytes, of the subresource data.

### -field SlicePitch

The slice pitch, or width, or physical size, in bytes, of the subresource data.

## -remarks

This structure is used by a number of helper methods, refer to <a href="/windows/desktop/direct3d12/helper-structures-and-functions-for-d3d12">Helper Structures and Functions for D3D12</a>.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>