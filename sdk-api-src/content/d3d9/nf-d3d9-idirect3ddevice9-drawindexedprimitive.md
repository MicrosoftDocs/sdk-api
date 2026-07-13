---
UID: NF:d3d9.IDirect3DDevice9.DrawIndexedPrimitive
title: IDirect3DDevice9::DrawIndexedPrimitive (d3d9.h)
description: The IDirect3DDevice9::DrawIndexedPrimitive method (d3d9.h) renders the specified geometric primitive into an array of vertices.
helpviewer_keywords: ["DrawIndexedPrimitive","DrawIndexedPrimitive method [Direct3D 9]","DrawIndexedPrimitive method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","DrawIndexedPrimitive method","IDirect3DDevice9.DrawIndexedPrimitive","IDirect3DDevice9::DrawIndexedPrimitive","a022738b-ecda-9413-683b-50134f542560","d3d9helper/IDirect3DDevice9::DrawIndexedPrimitive","direct3d9.idirect3ddevice9__drawindexedprimitive"]
old-location: direct3d9\idirect3ddevice9__drawindexedprimitive.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__drawindexedprimitive.htm
ms.date: 08/10/2022
ms.keywords: DrawIndexedPrimitive, DrawIndexedPrimitive method [Direct3D 9], DrawIndexedPrimitive method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],DrawIndexedPrimitive method, IDirect3DDevice9.DrawIndexedPrimitive, IDirect3DDevice9::DrawIndexedPrimitive, a022738b-ecda-9413-683b-50134f542560, d3d9helper/IDirect3DDevice9::DrawIndexedPrimitive, direct3d9.idirect3ddevice9__drawindexedprimitive
req.header: d3d9.h
req.include-header: D3D9.h
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
req.lib: D3D9.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirect3DDevice9::DrawIndexedPrimitive
 - d3d9/IDirect3DDevice9::DrawIndexedPrimitive
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DDevice9.DrawIndexedPrimitive
---

# IDirect3DDevice9::DrawIndexedPrimitive


## -description

Based on indexing, renders the specified geometric primitive into an array of vertices.

## -parameters

### -param unnamedParam1 [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dprimitivetype">D3DPRIMITIVETYPE</a></b>

Member of the <a href="/windows/desktop/direct3d9/d3dprimitivetype">D3DPRIMITIVETYPE</a> enumerated type, describing the type of primitive to render. D3DPT_POINTLIST is not supported with this method. See Remarks.

### -param BaseVertexIndex [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

Offset from the start of the vertex buffer to the first vertex. See <a href="/windows/desktop/direct3d9/rendering-from-vertex-and-index-buffers">Scenario 4</a>.

### -param MinVertexIndex [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Minimum vertex index for vertices used during this call. This is a zero based index relative to BaseVertexIndex.

### -param NumVertices [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of vertices used during this call. The first vertex is located at index: BaseVertexIndex + MinIndex.

### -param startIndex [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index of the first index to use when accessing the vertex buffer. Beginning at StartIndex to index vertices from the vertex buffer.

### -param primCount [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of primitives to render. The number of vertices used is a function of the primitive count and the primitive type. The maximum number of primitives allowed is determined by checking the MaxPrimitiveCount member of the <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9">D3DCAPS9</a> structure.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be the following:
     D3DERR_INVALIDCALL.

## -remarks

This method draws indexed primitives from the current set of data input streams. MinIndex  and all the indices in the index stream are relative to the BaseVertexIndex.

The MinIndex  and NumVertices  parameters specify the range of vertex indices used for each <b>IDirect3DDevice9::DrawIndexedPrimitive</b> call. These are used to optimize vertex processing of indexed primitives by processing a sequential range of vertices prior to indexing into these vertices. It is invalid for any indices used during this call to reference any vertices outside of this range.

<b>IDirect3DDevice9::DrawIndexedPrimitive</b> fails if no index array is set.

The D3DPT_POINTLIST member of the <a href="/windows/desktop/direct3d9/d3dprimitivetype">D3DPRIMITIVETYPE</a> enumerated type is not supported and is not a valid type for this method.

When converting a legacy application to Direct3D 9, you must add a call to either <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setfvf">IDirect3DDevice9::SetFVF</a> to use the fixed function pipeline, or <a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexdeclaration">IDirect3DDevice9::SetVertexDeclaration</a> to use a vertex shader before you make any Draw calls.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawprimitive">IDirect3DDevice9::DrawPrimitive</a>



<a href="/windows/desktop/direct3d9/index-buffers">Index Buffers (Direct3D 9)</a>



<a href="/windows/desktop/direct3d9/rendering-from-vertex-and-index-buffers">Rendering from Vertex and Index Buffers (Direct3D 9)</a>



<a href="/windows/desktop/direct3d9/vertex-buffers">Vertex Buffers (Direct3D 9)</a>
