---
UID: NF:d3d9.IDirect3DDevice9Ex.CreateOffscreenPlainSurfaceEx
title: IDirect3DDevice9Ex::CreateOffscreenPlainSurfaceEx (d3d9.h)
description: Create an off-screen surface. (IDirect3DDevice9Ex.CreateOffscreenPlainSurfaceEx)
helpviewer_keywords: ["63d121fa-1b4f-16db-b792-c30558006ddb","CreateOffscreenPlainSurfaceEx","CreateOffscreenPlainSurfaceEx method [Direct3D 9]","CreateOffscreenPlainSurfaceEx method [Direct3D 9]","IDirect3DDevice9Ex interface","IDirect3DDevice9Ex interface [Direct3D 9]","CreateOffscreenPlainSurfaceEx method","IDirect3DDevice9Ex.CreateOffscreenPlainSurfaceEx","IDirect3DDevice9Ex::CreateOffscreenPlainSurfaceEx","d3d9/IDirect3DDevice9Ex::CreateOffscreenPlainSurfaceEx","direct3d9.idirect3ddevice9ex_createoffscreenplainsurfaceex"]
old-location: direct3d9\idirect3ddevice9ex_createoffscreenplainsurfaceex.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9ex_createoffscreenplainsurfaceex.htm
ms.date: 12/05/2018
ms.keywords: 63d121fa-1b4f-16db-b792-c30558006ddb, CreateOffscreenPlainSurfaceEx, CreateOffscreenPlainSurfaceEx method [Direct3D 9], CreateOffscreenPlainSurfaceEx method [Direct3D 9],IDirect3DDevice9Ex interface, IDirect3DDevice9Ex interface [Direct3D 9],CreateOffscreenPlainSurfaceEx method, IDirect3DDevice9Ex.CreateOffscreenPlainSurfaceEx, IDirect3DDevice9Ex::CreateOffscreenPlainSurfaceEx, d3d9/IDirect3DDevice9Ex::CreateOffscreenPlainSurfaceEx, direct3d9.idirect3ddevice9ex_createoffscreenplainsurfaceex
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
 - IDirect3DDevice9Ex::CreateOffscreenPlainSurfaceEx
 - d3d9/IDirect3DDevice9Ex::CreateOffscreenPlainSurfaceEx
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
 - IDirect3DDevice9Ex.CreateOffscreenPlainSurfaceEx
---

# IDirect3DDevice9Ex::CreateOffscreenPlainSurfaceEx


## -description

Create an off-screen surface.

## -parameters

### -param Width [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Width of the surface.

### -param Height [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Height of the surface.

### -param Format [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a></b>

Format of the surface. See <a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a>.

### -param Pool [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dpool">D3DPOOL</a></b>

Surface pool type. See <a href="/windows/desktop/direct3d9/d3dpool">D3DPOOL</a>.

### -param ppSurface [out, retval]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a>**</b>

Pointer to the <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a>  interface created.

### -param pSharedHandle [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HANDLE</a>*</b>

Reserved. Set this parameter to <b>NULL</b>. This parameter can be used in Direct3D 9 for Windows Vista to <a href="/windows/desktop/direct3d9/dx9lh">share resources</a>.

### -param Usage [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Combination of one or more <a href="/windows/desktop/direct3d9/d3dusage">D3DUSAGE</a> constants which can be OR'd together. Value of 0 indicates no usage.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be the following:
     D3DERR_INVALIDCALL.

## -remarks

D3DPOOL_SCRATCH will return a surface that has identical characteristics to a surface created by the DirectX 8.x method CreateImageSurface.

D3DPOOL_DEFAULT is the appropriate pool for use with the <a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect">IDirect3DDevice9::StretchRect</a> and <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-colorfill">IDirect3DDevice9::ColorFill</a>.

D3DPOOL_MANAGED is not allowed when creating an offscreen plain surface. For more information about memory pools, see <a href="/windows/desktop/direct3d9/d3dpool">D3DPOOL</a>.

Off-screen plain surfaces are always lockable, regardless of their pool types.

## -see-also

<a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex">IDirect3DDevice9Ex</a>
