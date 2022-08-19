---
UID: NF:d3d9helper.IDirect3DDevice9.GetScissorRect
title: IDirect3DDevice9::GetScissorRect (d3d9helper.h)
description: The IDirect3DDevice9::GetScissorRect method (d3d9.h) gets the scissor rectangle.
helpviewer_keywords: ["7de78b9b-0918-15ce-f2b5-f1b433033d52","GetScissorRect","GetScissorRect method [Direct3D 9]","GetScissorRect method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","GetScissorRect method","IDirect3DDevice9.GetScissorRect","IDirect3DDevice9::GetScissorRect","d3d9helper/IDirect3DDevice9::GetScissorRect","direct3d9.idirect3ddevice9__getscissorrect"]
old-location: direct3d9\idirect3ddevice9__getscissorrect.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getscissorrect.htm
ms.date: 08/11/2022
ms.keywords: 7de78b9b-0918-15ce-f2b5-f1b433033d52, GetScissorRect, GetScissorRect method [Direct3D 9], GetScissorRect method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetScissorRect method, IDirect3DDevice9.GetScissorRect, IDirect3DDevice9::GetScissorRect, d3d9helper/IDirect3DDevice9::GetScissorRect, direct3d9.idirect3ddevice9__getscissorrect
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
 - IDirect3DDevice9::GetScissorRect
 - d3d9helper/IDirect3DDevice9::GetScissorRect
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
 - IDirect3DDevice9.GetScissorRect
---

# IDirect3DDevice9::GetScissorRect


## -description

Gets the scissor rectangle.

## -parameters

### -param pRect [out]

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

Returns a pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that defines the rendering area within the render target if scissor test is enabled.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be the following:
     D3DERR_INVALIDCALL.

## -remarks

The scissor rectangle is used as a rectangular clipping region.

See <a href="/windows/desktop/direct3d9/rectangles">Rectangles (Direct3D 9)</a> for further information on the use of rectangles in DirectX.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>
