---
UID: NE:d3d12.D3D12_DSV_FLAGS
title: D3D12_DSV_FLAGS (d3d12.h)
description: Specifies depth-stencil view options.
helpviewer_keywords: ["D3D12_DSV_FLAGS","D3D12_DSV_FLAGS enumeration","D3D12_DSV_FLAG_NONE","D3D12_DSV_FLAG_READ_ONLY_DEPTH","D3D12_DSV_FLAG_READ_ONLY_STENCIL","d3d12/D3D12_DSV_FLAGS","d3d12/D3D12_DSV_FLAG_NONE","d3d12/D3D12_DSV_FLAG_READ_ONLY_DEPTH","d3d12/D3D12_DSV_FLAG_READ_ONLY_STENCIL","direct3d12.d3d12_dsv_flags"]
old-location: direct3d12\d3d12_dsv_flags.htm
tech.root: direct3d12
ms.assetid: A968BFFF-8C26-4C8C-9AA4-7E9BB5B0DF1F
ms.date: 12/05/2018
ms.keywords: D3D12_DSV_FLAGS, D3D12_DSV_FLAGS enumeration, D3D12_DSV_FLAG_NONE, D3D12_DSV_FLAG_READ_ONLY_DEPTH, D3D12_DSV_FLAG_READ_ONLY_STENCIL, d3d12/D3D12_DSV_FLAGS, d3d12/D3D12_DSV_FLAG_NONE, d3d12/D3D12_DSV_FLAG_READ_ONLY_DEPTH, d3d12/D3D12_DSV_FLAG_READ_ONLY_STENCIL, direct3d12.d3d12_dsv_flags
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
req.typenames: D3D12_DSV_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_DSV_FLAGS
 - d3d12/D3D12_DSV_FLAGS
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
 - D3D12_DSV_FLAGS
---

# D3D12_DSV_FLAGS enumeration


## -description

Specifies depth-stencil view options.

## -enum-fields

### -field D3D12_DSV_FLAG_NONE:0

Indicates a default view.

### -field D3D12_DSV_FLAG_READ_ONLY_DEPTH:0x1

Indicates that depth values are read only.

### -field D3D12_DSV_FLAG_READ_ONLY_STENCIL:0x2

Indicates that stencil values are read only.

## -remarks

Specify a combination of the values in this enumeration in the <b>Flags</b> member of a <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_view_desc">D3D12_DEPTH_STENCIL_VIEW_DESC</a> structure.
          The values are combined by using a bitwise OR operation.
        

Limiting a depth-stencil buffer to read-only access allows more than one depth-stencil view to be bound to the pipeline simultaneously, since it is not possible to have read/write conflicts between separate views.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>
