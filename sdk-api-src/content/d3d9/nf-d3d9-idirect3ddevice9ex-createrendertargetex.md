---
UID: NF:d3d9.IDirect3DDevice9Ex.CreateRenderTargetEx
title: IDirect3DDevice9Ex::CreateRenderTargetEx (d3d9.h)
description: Creates a render-target surface. (IDirect3DDevice9Ex.CreateRenderTargetEx)
helpviewer_keywords: ["78a5ebad-c705-e895-65b2-37612b0e204e","CreateRenderTargetEx","CreateRenderTargetEx method [Direct3D 9]","CreateRenderTargetEx method [Direct3D 9]","IDirect3DDevice9Ex interface","IDirect3DDevice9Ex interface [Direct3D 9]","CreateRenderTargetEx method","IDirect3DDevice9Ex.CreateRenderTargetEx","IDirect3DDevice9Ex::CreateRenderTargetEx","d3d9/IDirect3DDevice9Ex::CreateRenderTargetEx","direct3d9.idirect3ddevice9ex_createrendertargetex"]
old-location: direct3d9\idirect3ddevice9ex_createrendertargetex.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9ex_createrendertargetex.htm
ms.date: 12/05/2018
ms.keywords: 78a5ebad-c705-e895-65b2-37612b0e204e, CreateRenderTargetEx, CreateRenderTargetEx method [Direct3D 9], CreateRenderTargetEx method [Direct3D 9],IDirect3DDevice9Ex interface, IDirect3DDevice9Ex interface [Direct3D 9],CreateRenderTargetEx method, IDirect3DDevice9Ex.CreateRenderTargetEx, IDirect3DDevice9Ex::CreateRenderTargetEx, d3d9/IDirect3DDevice9Ex::CreateRenderTargetEx, direct3d9.idirect3ddevice9ex_createrendertargetex
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
 - IDirect3DDevice9Ex::CreateRenderTargetEx
 - d3d9/IDirect3DDevice9Ex::CreateRenderTargetEx
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
 - IDirect3DDevice9Ex.CreateRenderTargetEx
---

# IDirect3DDevice9Ex::CreateRenderTargetEx


## -description

Creates a render-target surface.

## -parameters

### -param Width [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Width of the render-target surface, in pixels.

### -param Height [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Height of the render-target surface, in pixels.

### -param Format [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a></b>

Member of the <a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a> enumerated type, describing the format of the render target.

### -param MultiSample [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dmultisample-type">D3DMULTISAMPLE_TYPE</a></b>

Member of the <a href="/windows/desktop/direct3d9/d3dmultisample-type">D3DMULTISAMPLE_TYPE</a> enumerated type, which describes the multisampling buffer type. This parameter specifies the antialiasing type for this render target. When this surface is passed to <a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget">IDirect3DDevice9::SetRenderTarget</a>, its multisample type must be the same as that of the depth-stencil set by <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setdepthstencilsurface">IDirect3DDevice9::SetDepthStencilSurface</a>.

### -param MultisampleQuality [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Quality level. The valid range is between zero and one less than the level returned by pQualityLevels used by  <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype">IDirect3D9::CheckDeviceMultiSampleType</a>. Passing a larger value returns the error, D3DERR_INVALIDCALL. The MultisampleQuality values of paired render targets, depth stencil surfaces, and the multisample type must all match.

### -param Lockable [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Render targets are not lockable unless the application specifies <b>TRUE</b> for Lockable.

Note that lockable render targets reduce performance on some graphics hardware. The readback performance (moving data from video memory to system memory) depends on the type of hardware used (AGP vs. PCI Express) and is usually far lower than upload performance (moving data from system to video memory). If you need read access to render targets, use <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getrendertargetdata">GetRenderTargetData</a> instead of lockable render targets.

### -param ppSurface [out, retval]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a>**</b>

Address of a pointer to an <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a> interface.

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

Render-target surfaces are placed in the D3DPOOL_DEFAULT memory class.

The creation of lockable, multisampled render targets is not supported.

## -see-also

<a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex">IDirect3DDevice9Ex</a>
