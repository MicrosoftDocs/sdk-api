---
UID: NF:d3d9.IDirect3DDevice9.GetDepthStencilSurface
title: IDirect3DDevice9::GetDepthStencilSurface (d3d9.h)
description: The IDirect3DDevice9::GetDepthStencilSurface method (d3d9.h) gets the depth-stencil surface owned by the Direct3DDevice object.
helpviewer_keywords: ["838c2e61-ca4b-a0a4-7c79-dcedf679f8be","GetDepthStencilSurface","GetDepthStencilSurface method [Direct3D 9]","GetDepthStencilSurface method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","GetDepthStencilSurface method","IDirect3DDevice9.GetDepthStencilSurface","IDirect3DDevice9::GetDepthStencilSurface","d3d9helper/IDirect3DDevice9::GetDepthStencilSurface","direct3d9.idirect3ddevice9__getdepthstencilsurface"]
old-location: direct3d9\idirect3ddevice9__getdepthstencilsurface.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getdepthstencilsurface.htm
ms.date: 08/10/2022
ms.keywords: 838c2e61-ca4b-a0a4-7c79-dcedf679f8be, GetDepthStencilSurface, GetDepthStencilSurface method [Direct3D 9], GetDepthStencilSurface method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetDepthStencilSurface method, IDirect3DDevice9.GetDepthStencilSurface, IDirect3DDevice9::GetDepthStencilSurface, d3d9helper/IDirect3DDevice9::GetDepthStencilSurface, direct3d9.idirect3ddevice9__getdepthstencilsurface
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
 - IDirect3DDevice9::GetDepthStencilSurface
 - d3d9/IDirect3DDevice9::GetDepthStencilSurface
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
 - IDirect3DDevice9.GetDepthStencilSurface
---

# IDirect3DDevice9::GetDepthStencilSurface


## -description

Gets the depth-stencil surface owned by the Direct3DDevice object.

## -parameters

### -param ppZStencilSurface [out, retval]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a>**</b>

Address of a pointer to an <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a> interface, representing the returned depth-stencil surface.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK.If the device doesn't have a depth stencil buffer associated with it, the return value will be D3DERR_NOTFOUND. Otherwise, if the method fails, the return value can be D3DERR_INVALIDCALL.

## -remarks

Calling this method will increase the internal reference count on the <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a> interface. Failure to call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> when finished using this <b>IDirect3DSurface9</b> interface results in a memory leak.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setdepthstencilsurface">IDirect3DDevice9::SetDepthStencilSurface</a>
