---
UID: NF:d3d9.IDirect3DDevice9.DrawIndexedPrimitiveUP
title: IDirect3DDevice9::DrawIndexedPrimitiveUP (d3d9.h)
description: The IDirect3DDevice9::DrawIndexedPrimitiveUP method (d3d9.h) renders the specified geometric primitive with data specified by a user memory pointer. 
helpviewer_keywords: ["DrawIndexedPrimitiveUP","DrawIndexedPrimitiveUP method [Direct3D 9]","DrawIndexedPrimitiveUP method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","DrawIndexedPrimitiveUP method","IDirect3DDevice9.DrawIndexedPrimitiveUP","IDirect3DDevice9::DrawIndexedPrimitiveUP","a76e7ddd-b096-aabd-099d-4ef12355b8c1","d3d9helper/IDirect3DDevice9::DrawIndexedPrimitiveUP","direct3d9.idirect3ddevice9__drawindexedprimitiveup"]
old-location: direct3d9\idirect3ddevice9__drawindexedprimitiveup.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__drawindexedprimitiveup.htm
ms.date: 08/10/2022
ms.keywords: DrawIndexedPrimitiveUP, DrawIndexedPrimitiveUP method [Direct3D 9], DrawIndexedPrimitiveUP method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],DrawIndexedPrimitiveUP method, IDirect3DDevice9.DrawIndexedPrimitiveUP, IDirect3DDevice9::DrawIndexedPrimitiveUP, a76e7ddd-b096-aabd-099d-4ef12355b8c1, d3d9helper/IDirect3DDevice9::DrawIndexedPrimitiveUP, direct3d9.idirect3ddevice9__drawindexedprimitiveup
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
 - IDirect3DDevice9::DrawIndexedPrimitiveUP
 - d3d9/IDirect3DDevice9::DrawIndexedPrimitiveUP
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
 - IDirect3DDevice9.DrawIndexedPrimitiveUP
---

# IDirect3DDevice9::DrawIndexedPrimitiveUP


## -description

Renders the specified geometric primitive with data specified by a user memory pointer.

## -parameters

### -param PrimitiveType [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dprimitivetype">D3DPRIMITIVETYPE</a></b>

Member of the <a href="/windows/desktop/direct3d9/d3dprimitivetype">D3DPRIMITIVETYPE</a> enumerated type, describing the type of primitive to render.

### -param MinVertexIndex [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Minimum vertex index. This is a zero-based index.

### -param NumVertices [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

 Number of vertices used during this call. The first vertex is located at index: MinVertexIndex.

### -param PrimitiveCount [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of primitives to render. The maximum number of primitives allowed is determined by checking the MaxPrimitiveCount member of the <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9">D3DCAPS9</a> structure (the number of indices is a function of the primitive count and the primitive type).

### -param pIndexData [in]

Type: <b>const void*</b>

User memory pointer to the index data.

### -param IndexDataFormat [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a></b>

Member of the <a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a> enumerated type, describing the format of the index data. The valid settings are either: 


<ul>
<li>
<a href="/windows/desktop/direct3d9/d3dformat">D3DFMT_INDEX16</a>
</li>
<li>
<a href="/windows/desktop/direct3d9/d3dformat">D3DFMT_INDEX32</a>
</li>
</ul>

### -param pVertexStreamZeroData [in]

Type: <b>const void*</b>

User memory pointer to the vertex data. The vertex data must be in stream 0.

### -param VertexStreamZeroStride [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of bytes of data for each vertex. This value may not be 0.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be the following:
     D3DERR_INVALIDCALL.

## -remarks

This method is intended for use in applications that are unable to store their vertex data in vertex buffers. This method supports only a single vertex stream, which must be declared as stream 0.

Following any <b>IDirect3DDevice9::DrawIndexedPrimitiveUP</b> call, the stream 0 settings, referenced by <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getstreamsource">IDirect3DDevice9::GetStreamSource</a>, are set to <b>NULL</b>. Also, the index buffer setting for <a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setindices">IDirect3DDevice9::SetIndices</a> is set to <b>NULL</b>.

The vertex data passed to <b>IDirect3DDevice9::DrawIndexedPrimitiveUP</b> does not need to persist after the call. Direct3D completes its access to that data prior to returning from the call.

When converting a legacy application to Direct3D 9, you must add a call to either <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setfvf">IDirect3DDevice9::SetFVF</a> to use the fixed function pipeline, or <a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexdeclaration">IDirect3DDevice9::SetVertexDeclaration</a> to use a vertex shader before you make any Draw calls.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawprimitive">IDirect3DDevice9::DrawPrimitive</a>



<a href="/windows/desktop/direct3d9/rendering-from-vertex-and-index-buffers">Rendering from Vertex and Index Buffers (Direct3D 9)</a>
