---
UID: NF:d3d9.IDirect3DDevice9.DrawPrimitive
title: IDirect3DDevice9::DrawPrimitive (d3d9.h)
description: The IDirect3DDevice9::DrawPrimitive method (d3d9.h) renders a sequence of non-indexed, geometric primitives of the specified type from the current set of data input streams. 
helpviewer_keywords: ["DrawPrimitive","DrawPrimitive method [Direct3D 9]","DrawPrimitive method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","DrawPrimitive method","IDirect3DDevice9.DrawPrimitive","IDirect3DDevice9::DrawPrimitive","d3d9helper/IDirect3DDevice9::DrawPrimitive","direct3d9.idirect3ddevice9__drawprimitive","f6573fdd-1724-cbca-56a1-0b336470257e"]
old-location: direct3d9\idirect3ddevice9__drawprimitive.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__drawprimitive.htm
ms.date: 08/10/2022
ms.keywords: DrawPrimitive, DrawPrimitive method [Direct3D 9], DrawPrimitive method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],DrawPrimitive method, IDirect3DDevice9.DrawPrimitive, IDirect3DDevice9::DrawPrimitive, d3d9helper/IDirect3DDevice9::DrawPrimitive, direct3d9.idirect3ddevice9__drawprimitive, f6573fdd-1724-cbca-56a1-0b336470257e
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
 - IDirect3DDevice9::DrawPrimitive
 - d3d9/IDirect3DDevice9::DrawPrimitive
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
 - IDirect3DDevice9.DrawPrimitive
---

# IDirect3DDevice9::DrawPrimitive


## -description

Renders a sequence of nonindexed, geometric primitives of the specified type from the current set of data input streams.

## -parameters

### -param PrimitiveType [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dprimitivetype">D3DPRIMITIVETYPE</a></b>

Member of the <a href="/windows/desktop/direct3d9/d3dprimitivetype">D3DPRIMITIVETYPE</a> enumerated type, describing the type of primitive to render.

### -param StartVertex [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index of the first vertex to load. Beginning at StartVertex the correct number of vertices will be read out of the vertex buffer.

### -param PrimitiveCount [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of primitives to render. The maximum number of primitives allowed is determined by checking the MaxPrimitiveCount member of the <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9">D3DCAPS9</a> structure. PrimitiveCount is the number of primitives as determined by the primitive type. If it is a line list, each primitive has two vertices. If it is a triangle list, each primitive has three vertices.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be 
     D3DERR_INVALIDCALL.

## -remarks

When converting a legacy application to Direct3D 9, you must add a call to either <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setfvf">IDirect3DDevice9::SetFVF</a> to use the fixed function pipeline, or <a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexdeclaration">IDirect3DDevice9::SetVertexDeclaration</a> to use a vertex shader before you make any Draw calls.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawindexedprimitive">IDirect3DDevice9::DrawIndexedPrimitive</a>



<a href="/windows/desktop/direct3d9/rendering-from-vertex-and-index-buffers">Rendering from Vertex and Index Buffers (Direct3D 9)</a>
