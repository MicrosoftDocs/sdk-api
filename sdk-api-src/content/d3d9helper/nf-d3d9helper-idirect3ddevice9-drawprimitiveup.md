---
UID: NF:d3d9helper.IDirect3DDevice9.DrawPrimitiveUP
title: IDirect3DDevice9::DrawPrimitiveUP (d3d9helper.h)
description: The IDirect3DDevice9::DrawPrimitiveUP method (d3d9helper.h) renders data specified by a user memory pointer as a sequence of geometric primitives of the specified type.
helpviewer_keywords: ["3c41b201-e853-6403-545b-cddcebf45ea1","DrawPrimitiveUP","DrawPrimitiveUP method [Direct3D 9]","DrawPrimitiveUP method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","DrawPrimitiveUP method","IDirect3DDevice9.DrawPrimitiveUP","IDirect3DDevice9::DrawPrimitiveUP","d3d9helper/IDirect3DDevice9::DrawPrimitiveUP","direct3d9.idirect3ddevice9__drawprimitiveup"]
old-location: direct3d9\idirect3ddevice9__drawprimitiveup.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__drawprimitiveup.htm
ms.date: 08/11/2022
ms.keywords: 3c41b201-e853-6403-545b-cddcebf45ea1, DrawPrimitiveUP, DrawPrimitiveUP method [Direct3D 9], DrawPrimitiveUP method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],DrawPrimitiveUP method, IDirect3DDevice9.DrawPrimitiveUP, IDirect3DDevice9::DrawPrimitiveUP, d3d9helper/IDirect3DDevice9::DrawPrimitiveUP, direct3d9.idirect3ddevice9__drawprimitiveup
req.header: d3d9helper.h
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
 - IDirect3DDevice9::DrawPrimitiveUP
 - d3d9helper/IDirect3DDevice9::DrawPrimitiveUP
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
 - IDirect3DDevice9.DrawPrimitiveUP
---

# IDirect3DDevice9::DrawPrimitiveUP


## -description

Renders data specified by a user memory pointer as a sequence of geometric primitives of the specified type.

## -parameters

### -param PrimitiveType [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dprimitivetype">D3DPRIMITIVETYPE</a></b>

Member of the <a href="/windows/desktop/direct3d9/d3dprimitivetype">D3DPRIMITIVETYPE</a> enumerated type, describing the type of primitive to render.

### -param PrimitiveCount [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of primitives to render. The maximum number of primitives allowed is determined by checking the MaxPrimitiveCount member of the <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9">D3DCAPS9</a> structure.

### -param pVertexStreamZeroData [in]

Type: <b>const void*</b>

User memory pointer to the vertex data.

### -param VertexStreamZeroStride [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of bytes of data for each vertex. This value may not be 0.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be: D3DERR_INVALIDCALL.

## -remarks

This method is intended for use in applications that are unable to store their vertex data in vertex buffers. This method supports only a single vertex stream. The effect of this call is to use the provided vertex data pointer and stride for vertex stream 0. It is invalid to have the declaration of the current vertex shader refer to vertex streams other than stream 0.

Following any <b>IDirect3DDevice9::DrawPrimitiveUP</b> call, the stream 0 settings, referenced by <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getstreamsource">IDirect3DDevice9::GetStreamSource</a>, are set to <b>NULL</b>.

The vertex data passed to <b>IDirect3DDevice9::DrawPrimitiveUP</b> does not need to persist after the call. Direct3D completes its access to that data prior to returning from the call.

When converting a legacy application to Direct3D 9, you must add a call to either <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setfvf">IDirect3DDevice9::SetFVF</a> to use the fixed function pipeline, or <a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexdeclaration">IDirect3DDevice9::SetVertexDeclaration</a> to use a vertex shader before you make any Draw calls.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawindexedprimitiveup">IDirect3DDevice9::DrawIndexedPrimitiveUP</a>



<a href="/windows/desktop/direct3d9/rendering-from-vertex-and-index-buffers">Rendering from Vertex and Index Buffers (Direct3D 9)</a>
