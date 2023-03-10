---
UID: NF:d3d10.ID3D10Device.DrawInstanced
title: ID3D10Device::DrawInstanced (d3d10.h)
description: Draw non-indexed, instanced primitives. (ID3D10Device.DrawInstanced)
helpviewer_keywords: ["59daf614-be34-5946-a8e4-10a976e15345","DrawInstanced","DrawInstanced method [Direct3D 10]","DrawInstanced method [Direct3D 10]","ID3D10Device interface","ID3D10Device interface [Direct3D 10]","DrawInstanced method","ID3D10Device.DrawInstanced","ID3D10Device::DrawInstanced","d3d10/ID3D10Device::DrawInstanced","direct3d10.id3d10device_drawinstanced"]
old-location: direct3d10\id3d10device_drawinstanced.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_drawinstanced.htm
ms.date: 12/05/2018
ms.keywords: 59daf614-be34-5946-a8e4-10a976e15345, DrawInstanced, DrawInstanced method [Direct3D 10], DrawInstanced method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],DrawInstanced method, ID3D10Device.DrawInstanced, ID3D10Device::DrawInstanced, d3d10/ID3D10Device::DrawInstanced, direct3d10.id3d10device_drawinstanced
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
 - ID3D10Device::DrawInstanced
 - d3d10/ID3D10Device::DrawInstanced
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
 - ID3D10Device.DrawInstanced
---

# ID3D10Device::DrawInstanced


## -description

Draw non-indexed, instanced primitives.

## -parameters

### -param VertexCountPerInstance [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of vertices to draw.

### -param InstanceCount [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of instances to draw.

### -param StartVertexLocation [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index of the first vertex.

### -param StartInstanceLocation [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index of the first instance.

## -remarks

A <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-getting-started">draw API</a> submits work to the rendering pipeline.

Instancing may extend performance by reusing the same geometry to draw multiple objects in a scene. One example of instancing could be to draw the same object with different positions and colors. For an example of instancing, see the <a href="https://msdn.microsoft.com/library/Ee416415(v=VS.85).aspx">Instancing10 Sample</a>.

The vertex data for an instanced draw call normally comes from a vertex buffer that is bound to the pipeline. However, you could also provide the vertex data from a shader that has instanced data identified with a <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics">system-value semantic</a> (SV_InstanceID).

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
