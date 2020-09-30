---
UID: NS:d3d12.D3D12_CONSTANT_BUFFER_VIEW_DESC
title: D3D12_CONSTANT_BUFFER_VIEW_DESC (d3d12.h)
description: Describes a constant buffer to view.
helpviewer_keywords: ["D3D12_CONSTANT_BUFFER_VIEW_DESC","D3D12_CONSTANT_BUFFER_VIEW_DESC structure","d3d12/D3D12_CONSTANT_BUFFER_VIEW_DESC","direct3d12.d3d12_constant_buffer_view_desc"]
old-location: direct3d12\d3d12_constant_buffer_view_desc.htm
tech.root: direct3d12
ms.assetid: 83A4522E-AE87-42CE-9B95-CF63E92556AD
ms.date: 12/05/2018
ms.keywords: D3D12_CONSTANT_BUFFER_VIEW_DESC, D3D12_CONSTANT_BUFFER_VIEW_DESC structure, d3d12/D3D12_CONSTANT_BUFFER_VIEW_DESC, direct3d12.d3d12_constant_buffer_view_desc
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
req.typenames: D3D12_CONSTANT_BUFFER_VIEW_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_CONSTANT_BUFFER_VIEW_DESC
 - d3d12/D3D12_CONSTANT_BUFFER_VIEW_DESC
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
 - D3D12_CONSTANT_BUFFER_VIEW_DESC
---

# D3D12_CONSTANT_BUFFER_VIEW_DESC structure


## -description

Describes a constant buffer to view.

## -struct-fields

### -field BufferLocation

The D3D12_GPU_VIRTUAL_ADDRESS of the constant buffer.
            D3D12_GPU_VIRTUAL_ADDRESS is a typedef'd alias of UINT64.

### -field SizeInBytes

The size in bytes of the constant buffer.

## -remarks

This structure is used by <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview">CreateConstantBufferView</a>.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>