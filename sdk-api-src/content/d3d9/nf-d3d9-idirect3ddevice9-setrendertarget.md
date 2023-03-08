---
UID: NF:d3d9.IDirect3DDevice9.SetRenderTarget
title: IDirect3DDevice9::SetRenderTarget (d3d9.h)
description: The IDirect3DDevice9::SetRenderTarget method (d3d9helper.h) sets a new color buffer for the device.
helpviewer_keywords: ["8a35c59a-95b2-ac1b-0fde-a907c6a0b520","IDirect3DDevice9 interface [Direct3D 9]","SetRenderTarget method","IDirect3DDevice9.SetRenderTarget","IDirect3DDevice9::SetRenderTarget","SetRenderTarget","SetRenderTarget method [Direct3D 9]","SetRenderTarget method [Direct3D 9]","IDirect3DDevice9 interface","d3d9helper/IDirect3DDevice9::SetRenderTarget","direct3d9.idirect3ddevice9__setrendertarget"]
old-location: direct3d9\idirect3ddevice9__setrendertarget.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setrendertarget.htm
ms.date: 08/11/2022
ms.keywords: 8a35c59a-95b2-ac1b-0fde-a907c6a0b520, IDirect3DDevice9 interface [Direct3D 9],SetRenderTarget method, IDirect3DDevice9.SetRenderTarget, IDirect3DDevice9::SetRenderTarget, SetRenderTarget, SetRenderTarget method [Direct3D 9], SetRenderTarget method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::SetRenderTarget, direct3d9.idirect3ddevice9__setrendertarget
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
 - IDirect3DDevice9::SetRenderTarget
 - d3d9/IDirect3DDevice9::SetRenderTarget
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
 - IDirect3DDevice9.SetRenderTarget
---

# IDirect3DDevice9::SetRenderTarget


## -description

Sets a new color buffer for the device.

## -parameters

### -param RenderTargetIndex [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Index of the render target. See Remarks.

### -param pRenderTarget [in]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a>*</b>

Pointer to a new color buffer. If <b>NULL</b>, the color buffer for the corresponding RenderTargetIndex is disabled. Devices always must be associated with a color buffer.
 The new render-target surface must have at least D3DUSAGE_RENDERTARGET specified.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK.
 This method will return D3DERR_INVALIDCALL if either:


<ul>
<li>pRenderTarget = <b>NULL</b> and RenderTargetIndex = 0</li>
<li>pRenderTarget is != <b>NULL</b> and the render target is invalid.</li>
</ul>

## -remarks

The device can support multiple render targets. The number of render targets supported by a device is contained in the NumSimultaneousRTs member of <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9">D3DCAPS9</a>. See <a href="/windows/desktop/direct3d9/multiple-render-targets">Multiple Render Targets (Direct3D 9)</a>.

Setting a new render target will cause the viewport (see <a href="/windows/desktop/direct3d9/viewports-and-clipping">Viewports and Clipping (Direct3D 9)</a>) to be set to the full size of the new render target.

Some hardware tests the compatibility of the depth stencil buffer with the color buffer. If this is done, it is only done in a debug build.

Restrictions for using this method include the following:

<ul>
<li>The multisample type must be the same for the render target and the depth stencil surface.</li>
<li>The formats must be compatible for the render target and the depth stencil surface. See <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-checkdepthstencilmatch">IDirect3D9::CheckDepthStencilMatch</a>.</li>
<li>The size of the depth stencil surface must be greater than or equal to the size of the render target.</li>
</ul>
These restrictions are validated only when using the debug runtime when any of the <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>Draw methods are called.

Cube textures differ from other surfaces in that they are collections of surfaces. To call <b>IDirect3DDevice9::SetRenderTarget</b> with a cube texture, you must select an individual face using <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3dcubetexture9-getcubemapsurface">IDirect3DCubeTexture9::GetCubeMapSurface</a> and pass the resulting surface to <b>IDirect3DDevice9::SetRenderTarget</b>.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>
