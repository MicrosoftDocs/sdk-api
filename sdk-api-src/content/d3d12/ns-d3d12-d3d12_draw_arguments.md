---
UID: NS:d3d12.D3D12_DRAW_ARGUMENTS
title: D3D12_DRAW_ARGUMENTS (d3d12.h)
description: Describes parameters for drawing instances.
helpviewer_keywords: ["D3D12_DRAW_ARGUMENTS","D3D12_DRAW_ARGUMENTS structure","d3d12/D3D12_DRAW_ARGUMENTS","direct3d12.d3d12_draw_arguments"]
old-location: direct3d12\d3d12_draw_arguments.htm
tech.root: direct3d12
ms.assetid: 300F3628-C8E8-44BF-BCEC-579E6DA80347
ms.date: 12/05/2018
ms.keywords: D3D12_DRAW_ARGUMENTS, D3D12_DRAW_ARGUMENTS structure, d3d12/D3D12_DRAW_ARGUMENTS, direct3d12.d3d12_draw_arguments
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
req.typenames: D3D12_DRAW_ARGUMENTS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_DRAW_ARGUMENTS
 - d3d12/D3D12_DRAW_ARGUMENTS
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
 - D3D12_DRAW_ARGUMENTS
---

# D3D12_DRAW_ARGUMENTS structure


## -description

Describes parameters for drawing instances.

## -struct-fields

### -field VertexCountPerInstance

Specifies the number of vertices to draw, per instance.

### -field InstanceCount

Specifies the number of instances.

### -field StartVertexLocation

Specifies an index to the first vertex to start drawing from.

### -field StartInstanceLocation

Specifies an index to the first instance to start drawing from.

## -remarks

The members of this structure serve the same purpose as the parameters of  <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced">DrawInstanced</a>.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>