---
UID: NF:d3d9helper.IDirect3DDevice9.CreateDepthStencilSurface
title: IDirect3DDevice9::CreateDepthStencilSurface (d3d9helper.h)
description: The IDirect3DDevice9::CreateDepthStencilSurface method (d3d9helper.h) creates a depth-stencil resource.
helpviewer_keywords: ["16f106bf-8b42-ad75-370e-e0ecffdfcea5","CreateDepthStencilSurface","CreateDepthStencilSurface method [Direct3D 9]","CreateDepthStencilSurface method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","CreateDepthStencilSurface method","IDirect3DDevice9.CreateDepthStencilSurface","IDirect3DDevice9::CreateDepthStencilSurface","d3d9helper/IDirect3DDevice9::CreateDepthStencilSurface","direct3d9.idirect3ddevice9__createdepthstencilsurface"]
old-location: direct3d9\idirect3ddevice9__createdepthstencilsurface.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__createdepthstencilsurface.htm
ms.date: 08/11/2022
ms.keywords: 16f106bf-8b42-ad75-370e-e0ecffdfcea5, CreateDepthStencilSurface, CreateDepthStencilSurface method [Direct3D 9], CreateDepthStencilSurface method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],CreateDepthStencilSurface method, IDirect3DDevice9.CreateDepthStencilSurface, IDirect3DDevice9::CreateDepthStencilSurface, d3d9helper/IDirect3DDevice9::CreateDepthStencilSurface, direct3d9.idirect3ddevice9__createdepthstencilsurface
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
 - IDirect3DDevice9::CreateDepthStencilSurface
 - d3d9helper/IDirect3DDevice9::CreateDepthStencilSurface
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
 - IDirect3DDevice9.CreateDepthStencilSurface
---

# IDirect3DDevice9::CreateDepthStencilSurface


## -description

Creates a depth-stencil resource.

## -parameters

### -param Width [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Width of the depth-stencil surface, in pixels.

### -param Height [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Height of the depth-stencil surface, in pixels.

### -param Format [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a></b>

Member of the <a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a> enumerated type, describing the format of the depth-stencil surface. This value must be one of the enumerated depth-stencil formats for this device.

### -param MultiSample [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dmultisample-type">D3DMULTISAMPLE_TYPE</a></b>

Member of the <a href="/windows/desktop/direct3d9/d3dmultisample-type">D3DMULTISAMPLE_TYPE</a> enumerated type, describing the multisampling buffer type. This value must be one of the allowed multisample types. When this surface is passed to <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setdepthstencilsurface">IDirect3DDevice9::SetDepthStencilSurface</a>, its multisample type must be the same as that of the render target set by <a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget">IDirect3DDevice9::SetRenderTarget</a>.

### -param MultisampleQuality [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Quality level. The valid range is between zero and one less than the level returned by pQualityLevels used by  <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype">IDirect3D9::CheckDeviceMultiSampleType</a>. Passing a larger value returns the error D3DERR_INVALIDCALL. The MultisampleQuality values of paired render targets, depth stencil surfaces, and the MultiSample type must all match.

### -param Discard [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Set this flag to <b>TRUE</b> to enable z-buffer discarding, and <b>FALSE</b> otherwise.				
If this flag is set, the contents of the depth stencil buffer will be invalid after calling either <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-present">IDirect3DDevice9::Present</a> or <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setdepthstencilsurface">IDirect3DDevice9::SetDepthStencilSurface</a> with a different depth surface.

This flag has the same behavior as the constant,  D3DPRESENTFLAG_DISCARD_DEPTHSTENCIL, in <a href="/windows/desktop/direct3d9/d3dpresentflag">D3DPRESENTFLAG</a>.

### -param ppSurface [out, retval]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a>**</b>

Address of a pointer to an <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a> interface, representing the created depth-stencil surface resource.

### -param pSharedHandle [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HANDLE</a>*</b>

Reserved. Set this parameter to <b>NULL</b>. This parameter can be used in Direct3D 9 for Windows Vista to <a href="/windows/desktop/direct3d9/dx9lh">share resources</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_NOTAVAILABLE, D3DERR_INVALIDCALL, D3DERR_OUTOFVIDEOMEMORY, E_OUTOFMEMORY.

## -remarks

The memory class of the depth-stencil buffer is always D3DPOOL_DEFAULT.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatesurface">IDirect3DDevice9::UpdateSurface</a>
