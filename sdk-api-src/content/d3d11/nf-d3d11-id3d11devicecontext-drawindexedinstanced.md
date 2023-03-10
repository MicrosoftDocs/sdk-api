---
UID: NF:d3d11.ID3D11DeviceContext.DrawIndexedInstanced
title: ID3D11DeviceContext::DrawIndexedInstanced (d3d11.h)
description: Draw indexed, instanced primitives. (ID3D11DeviceContext.DrawIndexedInstanced)
helpviewer_keywords: ["8742ce56-5b31-7869-ab62-cb36d33cc5ca","DrawIndexedInstanced","DrawIndexedInstanced method [Direct3D 11]","DrawIndexedInstanced method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","DrawIndexedInstanced method","ID3D11DeviceContext.DrawIndexedInstanced","ID3D11DeviceContext::DrawIndexedInstanced","d3d11/ID3D11DeviceContext::DrawIndexedInstanced","direct3d11.id3d11devicecontext_drawindexedinstanced"]
old-location: direct3d11\id3d11devicecontext_drawindexedinstanced.htm
tech.root: direct3d11
ms.assetid: c7a4821a-324c-47e4-b89f-603d2afcfb51
ms.date: 12/05/2018
ms.keywords: 8742ce56-5b31-7869-ab62-cb36d33cc5ca, DrawIndexedInstanced, DrawIndexedInstanced method [Direct3D 11], DrawIndexedInstanced method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],DrawIndexedInstanced method, ID3D11DeviceContext.DrawIndexedInstanced, ID3D11DeviceContext::DrawIndexedInstanced, d3d11/ID3D11DeviceContext::DrawIndexedInstanced, direct3d11.id3d11devicecontext_drawindexedinstanced
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
 - ID3D11DeviceContext::DrawIndexedInstanced
 - d3d11/ID3D11DeviceContext::DrawIndexedInstanced
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
 - ID3D11DeviceContext.DrawIndexedInstanced
---

# ID3D11DeviceContext::DrawIndexedInstanced


## -description

Draw indexed, instanced primitives.

## -parameters

### -param IndexCountPerInstance [in]

Type: <b><a href="/windows/desktop/winprog/windows-data-types">UINT</a></b>

Number of indices read from the index buffer for each instance.

### -param InstanceCount [in]

Type: <b><a href="/windows/desktop/winprog/windows-data-types">UINT</a></b>

Number of instances to draw.

### -param StartIndexLocation [in]

Type: <b><a href="/windows/desktop/winprog/windows-data-types">UINT</a></b>

The location of the first index read by the GPU from the index buffer.

### -param BaseVertexLocation [in]

Type: <b><a href="/windows/desktop/winprog/windows-data-types">INT</a></b>

A value added to each index before reading a vertex from the vertex buffer.

### -param StartInstanceLocation [in]

Type: <b><a href="/windows/desktop/winprog/windows-data-types">UINT</a></b>

A value added to each index before reading per-instance data from a vertex buffer.

## -remarks

A draw API submits work to the rendering pipeline.

Instancing may extend performance by reusing the same geometry to draw multiple objects in a scene. One example of instancing could be to draw the same object with different positions and colors. Instancing requires multiple vertex buffers: at least one for per-vertex data and a second buffer for per-instance data.

The second buffer is needed only if the input layout that you use has elements that use [D3D11_INPUT_PER_INSTANCE_DATA](./ne-d3d11-d3d11_input_classification.md) as the input element classification buffer for per-instance data.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
