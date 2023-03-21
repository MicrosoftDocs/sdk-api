---
UID: NS:d3d12.D3D12_SUBRESOURCE_DATA
title: D3D12_SUBRESOURCE_DATA (d3d12.h)
description: Describes subresource data. (D3D12_SUBRESOURCE_DATA)
helpviewer_keywords: ["D3D12_SUBRESOURCE_DATA","D3D12_SUBRESOURCE_DATA structure","d3d12/D3D12_SUBRESOURCE_DATA","direct3d12.d3d12_subresource_data"]
old-location: direct3d12\d3d12_subresource_data.htm
tech.root: direct3d12
ms.assetid: A2749C3A-FD61-4775-8727-2D1CFC79A0F8
ms.date: 12/05/2018
ms.keywords: D3D12_SUBRESOURCE_DATA, D3D12_SUBRESOURCE_DATA structure, d3d12/D3D12_SUBRESOURCE_DATA, direct3d12.d3d12_subresource_data
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
req.typenames: D3D12_SUBRESOURCE_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_SUBRESOURCE_DATA
 - d3d12/D3D12_SUBRESOURCE_DATA
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
 - D3D12_SUBRESOURCE_DATA
---

# D3D12_SUBRESOURCE_DATA structure


## -description

Describes subresource data.

## -struct-fields

### -field pData

A pointer to a memory block that contains the subresource data.

### -field RowPitch

The row pitch, or width, or physical size, in bytes, of the subresource data.

### -field SlicePitch

The depth pitch, or width, or physical size, in bytes, of the subresource data.

## -remarks

This structure is used by a number of the helper functions, refer to <a href="/windows/desktop/direct3d12/helper-structures-and-functions-for-d3d12">Helper Structures and Functions for D3D12</a>.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>
