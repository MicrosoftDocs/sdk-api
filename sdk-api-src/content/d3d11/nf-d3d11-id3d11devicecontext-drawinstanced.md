---
UID: NF:d3d11.ID3D11DeviceContext.DrawInstanced
title: ID3D11DeviceContext::DrawInstanced (d3d11.h)
description: Draw non-indexed, instanced primitives. (ID3D11DeviceContext.DrawInstanced)
helpviewer_keywords: ["50e4d16f-22d4-d308-dcc8-fadbcf3a5568","DrawInstanced","DrawInstanced method [Direct3D 11]","DrawInstanced method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","DrawInstanced method","ID3D11DeviceContext.DrawInstanced","ID3D11DeviceContext::DrawInstanced","d3d11/ID3D11DeviceContext::DrawInstanced","direct3d11.id3d11devicecontext_drawinstanced"]
old-location: direct3d11\id3d11devicecontext_drawinstanced.htm
tech.root: direct3d11
ms.assetid: 3cb608e7-d64d-42cc-9b34-5f6c30af2ada
ms.date: 12/05/2018
ms.keywords: 50e4d16f-22d4-d308-dcc8-fadbcf3a5568, DrawInstanced, DrawInstanced method [Direct3D 11], DrawInstanced method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],DrawInstanced method, ID3D11DeviceContext.DrawInstanced, ID3D11DeviceContext::DrawInstanced, d3d11/ID3D11DeviceContext::DrawInstanced, direct3d11.id3d11devicecontext_drawinstanced
req.header: d3d11.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11DeviceContext::DrawInstanced
 - d3d11/ID3D11DeviceContext::DrawInstanced
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.DrawInstanced
---

# ID3D11DeviceContext::DrawInstanced


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

A value added to each index before reading per-instance data from a vertex buffer.

## -remarks

A draw API submits work to the rendering pipeline.

Instancing may extend performance by reusing the same geometry to draw multiple objects in a scene. One example of instancing could be 
      to draw the same object with different positions and colors.

The vertex data for an instanced draw call normally comes from a vertex buffer that is bound to the pipeline. 
      However, you could also provide the vertex data from a shader that has instanced data identified with a system-value semantic (SV_InstanceID).

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
