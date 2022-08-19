---
UID: NF:d3d9.IDirect3DTexture9.GetSurfaceLevel
title: IDirect3DTexture9::GetSurfaceLevel (d3d9.h)
description: The IDirect3DTexture9::GetSurfaceLevel (d3d9.h) method retrieves the specified texture surface level.
helpviewer_keywords: ["GetSurfaceLevel","GetSurfaceLevel method [Direct3D 9]","GetSurfaceLevel method [Direct3D 9]","IDirect3DTexture9 interface","IDirect3DTexture9 interface [Direct3D 9]","GetSurfaceLevel method","IDirect3DTexture9.GetSurfaceLevel","IDirect3DTexture9::GetSurfaceLevel","ba29c84a-8d60-aa0a-9eae-f64e0534c051","d3d9helper/IDirect3DTexture9::GetSurfaceLevel","direct3d9.idirect3dtexture9__getsurfacelevel"]
old-location: direct3d9\idirect3dtexture9__getsurfacelevel.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dtexture9__getsurfacelevel.htm
ms.date: 08/11/2022
ms.keywords: GetSurfaceLevel, GetSurfaceLevel method [Direct3D 9], GetSurfaceLevel method [Direct3D 9],IDirect3DTexture9 interface, IDirect3DTexture9 interface [Direct3D 9],GetSurfaceLevel method, IDirect3DTexture9.GetSurfaceLevel, IDirect3DTexture9::GetSurfaceLevel, ba29c84a-8d60-aa0a-9eae-f64e0534c051, d3d9helper/IDirect3DTexture9::GetSurfaceLevel, direct3d9.idirect3dtexture9__getsurfacelevel
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
 - IDirect3DTexture9::GetSurfaceLevel
 - d3d9/IDirect3DTexture9::GetSurfaceLevel
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
 - IDirect3DTexture9.GetSurfaceLevel
---

# IDirect3DTexture9::GetSurfaceLevel


## -description

Retrieves the specified texture surface level.

## -parameters

### -param Level [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Identifies a level of the texture resource. This method returns a surface for the level specified by this parameter. The top-level surface is denoted by 0.

### -param ppSurfaceLevel [out, retval]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a>**</b>

Address of a pointer to an <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a> interface, representing the returned surface.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one D3DERR_INVALIDCALL.

## -remarks

Calling this method will increase the internal reference count on the <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a> interface. Failure to call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> when finished using this <b>IDirect3DSurface9</b> interface results in a memory leak.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dtexture9">IDirect3DTexture9</a>
