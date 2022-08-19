---
UID: NF:d3d9helper.IDirect3DSurface9.GetDC
title: IDirect3DSurface9::GetDC (d3d9helper.h)
description: The IDirect3DSurface9::GetDC method (d3d9helper.h) retrieves a device context.
helpviewer_keywords: ["945f6e77-19f2-e9bf-18a4-09747a9990f3","GetDC","GetDC method [Direct3D 9]","GetDC method [Direct3D 9]","IDirect3DSurface9 interface","IDirect3DSurface9 interface [Direct3D 9]","GetDC method","IDirect3DSurface9.GetDC","IDirect3DSurface9::GetDC","d3d9helper/IDirect3DSurface9::GetDC","direct3d9.idirect3dsurface9__getdc"]
old-location: direct3d9\idirect3dsurface9__getdc.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dsurface9__getdc.htm
ms.date: 08/11/2022
ms.keywords: 945f6e77-19f2-e9bf-18a4-09747a9990f3, GetDC, GetDC method [Direct3D 9], GetDC method [Direct3D 9],IDirect3DSurface9 interface, IDirect3DSurface9 interface [Direct3D 9],GetDC method, IDirect3DSurface9.GetDC, IDirect3DSurface9::GetDC, d3d9helper/IDirect3DSurface9::GetDC, direct3d9.idirect3dsurface9__getdc
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
 - IDirect3DSurface9::GetDC
 - d3d9helper/IDirect3DSurface9::GetDC
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
 - IDirect3DSurface9.GetDC
---

# IDirect3DSurface9::GetDC


## -description

Retrieves a device context.

## -parameters

### -param phdc [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HDC</a>*</b>

Pointer to the device context for the surface.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. D3DERR_INVALIDCALL is returned if the argument is invalid.

## -remarks

The following restrictions apply.

<ul>
<li><b>IDirect3DSurface9::GetDC</b> is valid on the following formats only: D3DFMT_R5G6B5, D3DFMT_X1R5G5B5, D3DFMT_R8G8B8, and D3DFMT_X8R8G8B8. Formats that contain Alpha are not supported because the GDI implementations don't have a well-defined behavior on the alpha channel. For more information about formats, see <a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a>.</li>
<li>Only one device context per surface can be returned at a time.</li>
<li><b>IDirect3DSurface9::GetDC</b> will fail if the surface is already locked. If the surface is a member of a mipmap or cubemap, <b>IDirect3DSurface9::GetDC</b> fails if any other mipmap or cubemap member is locked.</li>
<li><b>IDirect3DSurface9::GetDC</b> fails on render targets unless they were created lockable (or, in the case of back buffers, with the D3DPRESENTFLAG_LOCKABLE_BACKBUFFER flag).</li>
<li>For surfaces not created with <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createoffscreenplainsurface">IDirect3DDevice9::CreateOffscreenPlainSurface</a>, <b>IDirect3DSurface9::GetDC</b> will fail on default pool (D3DPOOL_DEFAULT) surfaces unless they are dynamic (D3DUSAGE_DYNAMIC) or are lockable render targets.</li>
<li><b>IDirect3DSurface9::GetDC</b> will fail on D3DPOOL_SCRATCH surfaces.</li>
</ul>
When a device context is outstanding on a surface, the application may not call these methods:

<table>
<tr>
<td>IDirect3DCubeTexture9</td>
<td>
<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3dcubetexture9-lockrect">IDirect3DCubeTexture9::LockRect</a>
</td>
</tr>
<tr>
<td>IDirect3DDevice9</td>
<td>
<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-colorfill">IDirect3DDevice9::ColorFill</a>
</td>
</tr>
<tr>
<td></td>
<td>
<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect">IDirect3DDevice9::StretchRect</a>
</td>
</tr>
<tr>
<td></td>
<td>
<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatesurface">IDirect3DDevice9::UpdateSurface</a>
</td>
</tr>
<tr>
<td></td>
<td>
<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatetexture">IDirect3DDevice9::UpdateTexture</a>
</td>
</tr>
<tr>
<td>IDirect3DSurface9</td>
<td>
<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect">IDirect3DSurface9::LockRect</a>
</td>
</tr>
<tr>
<td>IDirect3DSwapChain9</td>
<td>
<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-present">IDirect3DSwapChain9::Present</a> *</td>
</tr>
<tr>
<td>IDirect3DTexture9</td>
<td>
<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-lockrect">IDirect3DTexture9::LockRect</a>
</td>
</tr>
</table>
 

* (on a swap chain that contains the surface)

<b>IDirect3DSurface9::GetDC</b> causes an implicit lock; do not retain the device context for later use. Call <a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-releasedc">IDirect3DSurface9::ReleaseDC</a> to release it.	

It is valid to call <b>IDirect3DSurface9::GetDC</b>/<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-releasedc">IDirect3DSurface9::ReleaseDC</a> on levels of a mipmap or cubemap, however, these calls will be slow to all miplevels except the topmost level, and GDI operations to these miplevels will not be accelerated.

The hdc provides access to Win32 and GDI functionality.

## -see-also

<a href="/windows/desktop/direct3d9/d3dpool">D3DPOOL</a>



<a href="/windows/desktop/direct3d9/d3dpresent-parameters">D3DPRESENT_PARAMETERS</a>



<a href="/windows/desktop/direct3d9/d3dusage">D3DUSAGE</a>



<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a>



<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-releasedc">IDirect3DSurface9::ReleaseDC</a>
