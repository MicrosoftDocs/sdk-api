---
UID: NF:d3d10.ID3D10Device.Draw
title: ID3D10Device::Draw (d3d10.h)
description: Draw non-indexed, non-instanced primitives. (ID3D10Device.Draw)
helpviewer_keywords: ["32601c9d-0f76-a5ab-559a-a11064280174","Draw","Draw method [Direct3D 10]","Draw method [Direct3D 10]","ID3D10Device interface","ID3D10Device interface [Direct3D 10]","Draw method","ID3D10Device.Draw","ID3D10Device::Draw","d3d10/ID3D10Device::Draw","direct3d10.id3d10device_draw"]
old-location: direct3d10\id3d10device_draw.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_draw.htm
ms.date: 12/05/2018
ms.keywords: 32601c9d-0f76-a5ab-559a-a11064280174, Draw, Draw method [Direct3D 10], Draw method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],Draw method, ID3D10Device.Draw, ID3D10Device::Draw, d3d10/ID3D10Device::Draw, direct3d10.id3d10device_draw
req.header: d3d10.h
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Device::Draw
 - d3d10/ID3D10Device::Draw
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.Draw
---

# ID3D10Device::Draw


## -description

Draw non-indexed, non-instanced primitives.

## -parameters

### -param VertexCount [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of vertices to draw.

### -param StartVertexLocation [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index of the first vertex, which is usually an offset in a vertex buffer; it could also be used as the first vertex id generated for a shader parameter marked with the <b>SV_TargetId</b> <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics">system-value semantic</a>.

## -remarks

A <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-getting-started">draw API</a> submits work to the rendering pipeline.

The vertex data for a draw call normally comes from a vertex buffer that is bound to the pipeline. However, you could also provide the vertex data from a shader that has vertex data marked with the <b>SV_VertexId</b> <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics">system-value semantic</a>.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
