---
UID: NF:d3d9helper.IDirect3DDevice9.SetDepthStencilSurface
title: IDirect3DDevice9::SetDepthStencilSurface (d3d9helper.h)
description: The IDirect3DDevice9::SetDepthStencilSurface method (d3d9.h) sets the depth stencil surface.
helpviewer_keywords: ["IDirect3DDevice9 interface [Direct3D 9]","SetDepthStencilSurface method","IDirect3DDevice9.SetDepthStencilSurface","IDirect3DDevice9::SetDepthStencilSurface","SetDepthStencilSurface","SetDepthStencilSurface method [Direct3D 9]","SetDepthStencilSurface method [Direct3D 9]","IDirect3DDevice9 interface","c973ddb0-10a2-26b2-bf86-57867238343e","d3d9helper/IDirect3DDevice9::SetDepthStencilSurface","direct3d9.idirect3ddevice9__setdepthstencilsurface"]
old-location: direct3d9\idirect3ddevice9__setdepthstencilsurface.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setdepthstencilsurface.htm
ms.date: 08/11/2022
ms.keywords: IDirect3DDevice9 interface [Direct3D 9],SetDepthStencilSurface method, IDirect3DDevice9.SetDepthStencilSurface, IDirect3DDevice9::SetDepthStencilSurface, SetDepthStencilSurface, SetDepthStencilSurface method [Direct3D 9], SetDepthStencilSurface method [Direct3D 9],IDirect3DDevice9 interface, c973ddb0-10a2-26b2-bf86-57867238343e, d3d9helper/IDirect3DDevice9::SetDepthStencilSurface, direct3d9.idirect3ddevice9__setdepthstencilsurface
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
 - IDirect3DDevice9::SetDepthStencilSurface
 - d3d9helper/IDirect3DDevice9::SetDepthStencilSurface
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
 - IDirect3DDevice9.SetDepthStencilSurface
---

# IDirect3DDevice9::SetDepthStencilSurface


## -description

Sets the depth stencil surface.

## -parameters

### -param pNewZStencil [in]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a>*</b>

Address of a pointer to an <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a> interface representing the depth stencil surface. Setting this to <b>NULL</b> disables the depth stencil operation.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK.
 If pZStencilSurface is other than <b>NULL</b>, the return value is D3DERR_INVALIDCALL when the stencil surface is invalid.

## -remarks

Restrictions for using this method include the following:

<ul>
<li>The multisample type must be the same for the render target and the depth stencil surface.</li>
<li>The formats must be compatible for the render target and the depth stencil surface. See <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-checkdepthstencilmatch">IDirect3D9::CheckDepthStencilMatch</a>.</li>
<li>The size of the depth stencil surface must be greater than or equal to the size of the render target.</li>
</ul>
These restrictions are validated only when using the debug runtime when any of the <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>Draw methods are called.

Cube textures differ from other surfaces in that they are collections of surfaces. To call <b>IDirect3DDevice9::SetDepthStencilSurface</b> with a cube texture, you must select an individual face using <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3dcubetexture9-getcubemapsurface">IDirect3DCubeTexture9::GetCubeMapSurface</a> and pass the resulting surface to <b>IDirect3DDevice9::SetDepthStencilSurface</b>.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getdepthstencilsurface">IDirect3DDevice9::GetDepthStencilSurface</a>
