---
UID: NF:d3d9helper.IDirect3DDevice9.GetStreamSource
title: IDirect3DDevice9::GetStreamSource (d3d9helper.h)
description: The IDirect3DDevice9::GetStreamSource method (d3d9.h) retrieves a vertex buffer bound to the specified data stream.
helpviewer_keywords: ["2e39bbb7-4148-9989-c1b0-1c60594bdf41","GetStreamSource","GetStreamSource method [Direct3D 9]","GetStreamSource method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","GetStreamSource method","IDirect3DDevice9.GetStreamSource","IDirect3DDevice9::GetStreamSource","d3d9helper/IDirect3DDevice9::GetStreamSource","direct3d9.idirect3ddevice9__getstreamsource"]
old-location: direct3d9\idirect3ddevice9__getstreamsource.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getstreamsource.htm
ms.date: 08/11/2022
ms.keywords: 2e39bbb7-4148-9989-c1b0-1c60594bdf41, GetStreamSource, GetStreamSource method [Direct3D 9], GetStreamSource method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetStreamSource method, IDirect3DDevice9.GetStreamSource, IDirect3DDevice9::GetStreamSource, d3d9helper/IDirect3DDevice9::GetStreamSource, direct3d9.idirect3ddevice9__getstreamsource
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
 - IDirect3DDevice9::GetStreamSource
 - d3d9helper/IDirect3DDevice9::GetStreamSource
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
 - IDirect3DDevice9.GetStreamSource
---

## -description

Retrieves a vertex buffer bound to the specified data stream.

## -parameters

### -param StreamNumber

Type: [in] <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Specifies the data stream, in the range from 0 to the maximum number of streams minus one.

### -param ppStreamData

Type: [in, out] <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9">IDirect3DVertexBuffer9</a>**</b>

Address of a pointer to an <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9">IDirect3DVertexBuffer9</a> interface, representing the returned vertex buffer bound to the specified data stream.

### -param OffsetInBytes

Type: [out] <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

Pointer containing the offset from the beginning of the stream to the beginning of the vertex data. The offset is measured in bytes. See Remarks.

### -param pStride

Type: [out] <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

Pointer to a returned stride of the component, in bytes. See Remarks.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.

## -remarks

A stream is defined as a uniform array of component data, where each component consists of one or more elements representing a single entity such as position, normal, color, and so on.

When a FVF vertex shader is used, the stride of the vertex stream must match the vertex size, computed from the FVF. When a declaration is used, the stride should be greater than or equal to the stream size computed from the declaration.

Calling this method increases the internal reference count on the <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9">IDirect3DVertexBuffer9</a> interface. Failure to call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> when finished using this <b>IDirect3DVertexBuffer9</b> interface results in a memory leak.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>

<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawindexedprimitive">IDirect3DDevice9::DrawIndexedPrimitive</a>

<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawindexedprimitiveup">IDirect3DDevice9::DrawIndexedPrimitiveUP</a>

<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawprimitive">IDirect3DDevice9::DrawPrimitive</a>

<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawprimitiveup">IDirect3DDevice9::DrawPrimitiveUP</a>

<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource">IDirect3DDevice9::SetStreamSource</a>

<a href="/windows/desktop/direct3d9/vertex-buffers">Vertex Buffers (Direct3D 9)</a>
