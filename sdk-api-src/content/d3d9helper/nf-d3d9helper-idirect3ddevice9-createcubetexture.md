---
UID: NF:d3d9helper.IDirect3DDevice9.CreateCubeTexture
title: IDirect3DDevice9::CreateCubeTexture (d3d9helper.h)
description: The IDirect3DDevice9::CreateCubeTexture method (d3d9helper.h) creates a cube texture resource.
helpviewer_keywords: ["0b1afd24-65fb-4a7c-77ef-c3b832e6d5f1","CreateCubeTexture","CreateCubeTexture method [Direct3D 9]","CreateCubeTexture method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","CreateCubeTexture method","IDirect3DDevice9.CreateCubeTexture","IDirect3DDevice9::CreateCubeTexture","d3d9helper/IDirect3DDevice9::CreateCubeTexture","direct3d9.idirect3ddevice9__createcubetexture"]
old-location: direct3d9\idirect3ddevice9__createcubetexture.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__createcubetexture.htm
ms.date: 08/11/2022
ms.keywords: 0b1afd24-65fb-4a7c-77ef-c3b832e6d5f1, CreateCubeTexture, CreateCubeTexture method [Direct3D 9], CreateCubeTexture method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],CreateCubeTexture method, IDirect3DDevice9.CreateCubeTexture, IDirect3DDevice9::CreateCubeTexture, d3d9helper/IDirect3DDevice9::CreateCubeTexture, direct3d9.idirect3ddevice9__createcubetexture
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
 - IDirect3DDevice9::CreateCubeTexture
 - d3d9helper/IDirect3DDevice9::CreateCubeTexture
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
 - IDirect3DDevice9.CreateCubeTexture
---

# IDirect3DDevice9::CreateCubeTexture


## -description

Creates a cube texture resource.

## -parameters

### -param EdgeLength [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Size of the edges of all the top-level faces of the cube texture. The pixel dimensions of subsequent levels of each face will be the truncated value of half of the previous level's pixel dimension (independently). Each dimension clamps at a size of 1 pixel. Thus, if the division by 2 results in 0 (zero), 1 will be taken instead.

### -param Levels [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of levels in each face of the cube texture. If this is zero, Direct3D will generate all cube texture sublevels down to 1x1 pixels for each face for hardware that supports mipmapped cube textures.  Call <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3dbasetexture9-getlevelcount">IDirect3DBaseTexture9::GetLevelCount</a> to see the number of levels generated.

### -param Usage [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Usage can be 0, which indicates no usage value. However, if usage is desired, use a combination of one or more <a href="/windows/desktop/direct3d9/d3dusage">D3DUSAGE</a> constants. It is good practice to match the usage parameter in CreateCubeTexture with the behavior flags in <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-createdevice">IDirect3D9::CreateDevice</a>. For more information, see Remarks.

### -param Format [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a></b>

Member of the <a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a> enumerated type, describing the format of all levels in all faces of the cube texture.

### -param Pool [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dpool">D3DPOOL</a></b>

Member of the <a href="/windows/desktop/direct3d9/d3dpool">D3DPOOL</a> enumerated type, describing the memory class into which the cube texture should be placed.

### -param ppCubeTexture [out, retval]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9">IDirect3DCubeTexture9</a>**</b>

Address of a pointer to an <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9">IDirect3DCubeTexture9</a> interface, representing the created cube texture resource.

### -param pSharedHandle [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HANDLE</a>*</b>

Reserved. Set this parameter to <b>NULL</b>. This parameter can be used in Direct3D 9 for Windows Vista to <a href="/windows/desktop/direct3d9/dx9lh">share resources</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_INVALIDCALL, D3DERR_OUTOFVIDEOMEMORY, E_OUTOFMEMORY.

## -remarks

A mipmap (texture) is a collection of successively downsampled (mipmapped) surfaces. On the other hand, a cube texture (created by <b>IDirect3DDevice9::CreateCubeTexture</b>) is a collection of six textures (mipmaps), one for each face. All faces must be present in the cube texture. Also, a cube map surface must be the same pixel size in all three dimensions (x, y, and z).

An application can discover support for <a href="/windows/desktop/direct3d9/automatic-generation-of-mipmaps">Automatic Generation of Mipmaps (Direct3D 9)</a> in a particular format by calling <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat">IDirect3D9::CheckDeviceFormat</a> with D3DUSAGE_AUTOGENMIPMAP. If <b>IDirect3D9::CheckDeviceFormat</b> returns D3DOK_NOAUTOGEN, <b>IDirect3DDevice9::CreateCubeTexture</b> will succeed but it will return a one-level texture.

## -see-also

<a href="/windows/desktop/direct3d9/d3dxcreatecubetexture">D3DXCreateCubeTexture</a>



<a href="/windows/desktop/direct3d9/d3dxcreatecubetexturefromfile">D3DXCreateCubeTextureFromFile</a>



<a href="/windows/desktop/direct3d9/d3dxcreatecubetexturefromfileex">D3DXCreateCubeTextureFromFileEx</a>



<a href="/windows/desktop/direct3d9/d3dxcreatecubetexturefromfileinmemory">D3DXCreateCubeTextureFromFileInMemory</a>



<a href="/windows/desktop/direct3d9/d3dxcreatecubetexturefromfileinmemoryex">D3DXCreateCubeTextureFromFileInMemoryEx</a>



<a href="/windows/desktop/direct3d9/d3dxcreatecubetexturefromresource">D3DXCreateCubeTextureFromResource</a>



<a href="/windows/desktop/direct3d9/d3dxcreatecubetexturefromresourceex">D3DXCreateCubeTextureFromResourceEx</a>



<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>
