---
UID: NF:d3d9.IDirect3DDevice9Ex.CreateDepthStencilSurfaceEx
title: IDirect3DDevice9Ex::CreateDepthStencilSurfaceEx (d3d9.h)
description: Creates a depth-stencil surface.
helpviewer_keywords: ["CreateDepthStencilSurfaceEx","CreateDepthStencilSurfaceEx method [Direct3D 9]","CreateDepthStencilSurfaceEx method [Direct3D 9]","IDirect3DDevice9Ex interface","IDirect3DDevice9Ex interface [Direct3D 9]","CreateDepthStencilSurfaceEx method","IDirect3DDevice9Ex.CreateDepthStencilSurfaceEx","IDirect3DDevice9Ex::CreateDepthStencilSurfaceEx","cba58342-5f61-5670-e0b8-8fe6a23a5130","d3d9/IDirect3DDevice9Ex::CreateDepthStencilSurfaceEx","direct3d9.idirect3ddevice9ex_createdepthstencilsurfaceex"]
old-location: direct3d9\idirect3ddevice9ex_createdepthstencilsurfaceex.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9ex_createdepthstencilsurfaceex.htm
ms.date: 12/05/2018
ms.keywords: CreateDepthStencilSurfaceEx, CreateDepthStencilSurfaceEx method [Direct3D 9], CreateDepthStencilSurfaceEx method [Direct3D 9],IDirect3DDevice9Ex interface, IDirect3DDevice9Ex interface [Direct3D 9],CreateDepthStencilSurfaceEx method, IDirect3DDevice9Ex.CreateDepthStencilSurfaceEx, IDirect3DDevice9Ex::CreateDepthStencilSurfaceEx, cba58342-5f61-5670-e0b8-8fe6a23a5130, d3d9/IDirect3DDevice9Ex::CreateDepthStencilSurfaceEx, direct3d9.idirect3ddevice9ex_createdepthstencilsurfaceex
req.header: d3d9.h
req.include-header: 
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
 - IDirect3DDevice9Ex::CreateDepthStencilSurfaceEx
 - d3d9/IDirect3DDevice9Ex::CreateDepthStencilSurfaceEx
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
 - IDirect3DDevice9Ex.CreateDepthStencilSurfaceEx
---

# IDirect3DDevice9Ex::CreateDepthStencilSurfaceEx


## -description

Creates a depth-stencil surface.

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

### -param Usage [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Combination of one or more <a href="/windows/desktop/direct3d9/d3dusage">D3DUSAGE</a> constants which can be OR'd together. Value of 0 indicates no usage.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_NOTAVAILABLE, D3DERR_INVALIDCALL, D3DERR_OUTOFVIDEOMEMORY, E_OUTOFMEMORY.

## -remarks

The memory class of the depth-stencil buffer is always D3DPOOL_DEFAULT.

## -see-also

<a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex">IDirect3DDevice9Ex</a>