---
UID: NF:d3d9.IDirect3DDevice9.SetIndices
title: IDirect3DDevice9::SetIndices (d3d9.h)
description: The IDirect3DDevice9::SetIndices method (d3d9.h) sets index data.
helpviewer_keywords: ["IDirect3DDevice9 interface [Direct3D 9]","SetIndices method","IDirect3DDevice9.SetIndices","IDirect3DDevice9::SetIndices","SetIndices","SetIndices method [Direct3D 9]","SetIndices method [Direct3D 9]","IDirect3DDevice9 interface","d3d9helper/IDirect3DDevice9::SetIndices","direct3d9.idirect3ddevice9__setindices","f1b39c78-eab2-fb54-c553-da8d9f26d06b"]
old-location: direct3d9\idirect3ddevice9__setindices.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setindices.htm
ms.date: 08/11/2022
ms.keywords: IDirect3DDevice9 interface [Direct3D 9],SetIndices method, IDirect3DDevice9.SetIndices, IDirect3DDevice9::SetIndices, SetIndices, SetIndices method [Direct3D 9], SetIndices method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::SetIndices, direct3d9.idirect3ddevice9__setindices, f1b39c78-eab2-fb54-c553-da8d9f26d06b
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
 - IDirect3DDevice9::SetIndices
 - d3d9/IDirect3DDevice9::SetIndices
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
 - IDirect3DDevice9.SetIndices
---

# IDirect3DDevice9::SetIndices


## -description

Sets index data.

## -parameters

### -param pIndexData [in]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9">IDirect3DIndexBuffer9</a>*</b>

Pointer to an <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9">IDirect3DIndexBuffer9</a> interface, representing the index data to be set.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be: D3DERR_INVALIDCALL.

## -remarks

When an application no longer holds a references to this interface, the interface will automatically be freed.

The <b>IDirect3DDevice9::SetIndices</b> method sets the current index array to an index buffer. The single set of indices is used to index all streams.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawindexedprimitive">IDirect3DDevice9::DrawIndexedPrimitive</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawindexedprimitiveup">IDirect3DDevice9::DrawIndexedPrimitiveUP</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawprimitive">IDirect3DDevice9::DrawPrimitive</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawprimitiveup">IDirect3DDevice9::DrawPrimitiveUP</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getindices">IDirect3DDevice9::GetIndices</a>



<a href="/windows/desktop/direct3d9/index-buffers">Index Buffers (Direct3D 9)</a>
