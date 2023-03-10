---
UID: NF:d3d9helper.IDirect3DCubeTexture9.GetCubeMapSurface
title: IDirect3DCubeTexture9::GetCubeMapSurface (d3d9helper.h)
description: The IDirect3DCubeTexture9::GetCubeMapSurface method (d3d9.h) retrieves a cube texture map surface.
helpviewer_keywords: ["6704f537-4e72-4fb1-e408-561e7971fd8f","GetCubeMapSurface","GetCubeMapSurface method [Direct3D 9]","GetCubeMapSurface method [Direct3D 9]","IDirect3DCubeTexture9 interface","IDirect3DCubeTexture9 interface [Direct3D 9]","GetCubeMapSurface method","IDirect3DCubeTexture9.GetCubeMapSurface","IDirect3DCubeTexture9::GetCubeMapSurface","d3d9helper/IDirect3DCubeTexture9::GetCubeMapSurface","direct3d9.idirect3dcubetexture9__getcubemapsurface"]
old-location: direct3d9\idirect3dcubetexture9__getcubemapsurface.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dcubetexture9__getcubemapsurface.htm
ms.date: 08/11/2022
ms.keywords: 6704f537-4e72-4fb1-e408-561e7971fd8f, GetCubeMapSurface, GetCubeMapSurface method [Direct3D 9], GetCubeMapSurface method [Direct3D 9],IDirect3DCubeTexture9 interface, IDirect3DCubeTexture9 interface [Direct3D 9],GetCubeMapSurface method, IDirect3DCubeTexture9.GetCubeMapSurface, IDirect3DCubeTexture9::GetCubeMapSurface, d3d9helper/IDirect3DCubeTexture9::GetCubeMapSurface, direct3d9.idirect3dcubetexture9__getcubemapsurface
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
 - IDirect3DCubeTexture9::GetCubeMapSurface
 - d3d9helper/IDirect3DCubeTexture9::GetCubeMapSurface
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
 - IDirect3DCubeTexture9.GetCubeMapSurface
---

# IDirect3DCubeTexture9::GetCubeMapSurface


## -description

Retrieves a cube texture map surface.

## -parameters

### -param FaceType [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dcubemap-faces">D3DCUBEMAP_FACES</a></b>

Member of the <a href="/windows/desktop/direct3d9/d3dcubemap-faces">D3DCUBEMAP_FACES</a> enumerated type, identifying a cube map face.

### -param Level [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Specifies a level of a mipmapped cube texture.

### -param ppCubeMapSurface [out]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a>**</b>

Address of a pointer to an <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a> interface, representing the returned cube texture map surface.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be: D3DERR_INVALIDCALL.

## -remarks

Calling this method will increase the internal reference count on the <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a> interface. Failure to call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> when finished using this <b>IDirect3DSurface9</b> interface results in a memory leak.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9">IDirect3DCubeTexture9</a>
