---
UID: NF:d3d9helper.IDirect3DDevice9.CreateVolumeTexture
title: IDirect3DDevice9::CreateVolumeTexture (d3d9helper.h)
description: The IDirect3DDevice9::CreateVolumeTexture method (d3d9helper.h) creates a volume texture resource.
helpviewer_keywords: ["CreateVolumeTexture","CreateVolumeTexture method [Direct3D 9]","CreateVolumeTexture method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","CreateVolumeTexture method","IDirect3DDevice9.CreateVolumeTexture","IDirect3DDevice9::CreateVolumeTexture","d27be66d-3b8c-f3af-34b8-9478b75f7b15","d3d9helper/IDirect3DDevice9::CreateVolumeTexture","direct3d9.idirect3ddevice9__createvolumetexture"]
old-location: direct3d9\idirect3ddevice9__createvolumetexture.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__createvolumetexture.htm
ms.date: 08/11/2022
ms.keywords: CreateVolumeTexture, CreateVolumeTexture method [Direct3D 9], CreateVolumeTexture method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],CreateVolumeTexture method, IDirect3DDevice9.CreateVolumeTexture, IDirect3DDevice9::CreateVolumeTexture, d27be66d-3b8c-f3af-34b8-9478b75f7b15, d3d9helper/IDirect3DDevice9::CreateVolumeTexture, direct3d9.idirect3ddevice9__createvolumetexture
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
 - IDirect3DDevice9::CreateVolumeTexture
 - d3d9helper/IDirect3DDevice9::CreateVolumeTexture
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
 - IDirect3DDevice9.CreateVolumeTexture
---

# IDirect3DDevice9::CreateVolumeTexture


## -description

Creates a volume texture resource.

## -parameters

### -param Width [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Width of the top-level of the volume texture, in pixels. This value must be a power of two if the D3DPTEXTURECAPS_VOLUMEMAP_POW2 member of <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9">D3DCAPS9</a> is set. The pixel dimensions of subsequent levels will be the truncated value of half of the previous level's pixel dimension (independently). Each dimension clamps at a size of 1 pixel. Thus, if the division by two results in 0 (zero), 1 will be taken instead. The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in <b>D3DCAPS9</b>.

### -param Height [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Height of the top-level of the volume texture, in pixels. This value must be a power of two if the D3DPTEXTURECAPS_VOLUMEMAP_POW2 member of <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9">D3DCAPS9</a> is set. The pixel dimensions of subsequent levels will be the truncated value of half of the previous level's pixel dimension (independently). Each dimension clamps at a size of 1 pixel. Thus, if the division by 2 results in 0 (zero), 1 will be taken instead. The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in <b>D3DCAPS9</b>.

### -param Depth [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Depth of the top-level of the volume texture, in pixels. This value must be a power of two if the D3DPTEXTURECAPS_VOLUMEMAP_POW2 member of <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9">D3DCAPS9</a> is set. The pixel dimensions of subsequent levels will be the truncated value of half of the previous level's pixel dimension (independently). Each dimension clamps at a size of 1 pixel. Thus, if the division by 2 results in 0 (zero), 1 will be taken instead. The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in <b>D3DCAPS9</b>.

### -param Levels [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of levels in the texture. If this is zero, Direct3D will generate all texture sublevels down to 1x1 pixels for hardware that supports mipmapped volume textures. Call <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3dbasetexture9-getlevelcount">IDirect3DBaseTexture9::GetLevelCount</a> to see the number of levels generated.

### -param Usage [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Usage can be 0, which indicates no usage value. If usage is desired, use D3DUSAGE_DYNAMIC or D3DUSAGE_SOFTWAREPROCESSING. For more information, see <a href="/windows/desktop/direct3d9/d3dusage">D3DUSAGE</a>.

### -param Format [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a></b>

Member of the <a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a> enumerated type, describing the format of all levels in the volume texture.

### -param Pool [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dpool">D3DPOOL</a></b>

Member of the <a href="/windows/desktop/direct3d9/d3dpool">D3DPOOL</a> enumerated type, describing the memory class into which the volume texture should be placed.

### -param ppVolumeTexture [out, retval]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9">IDirect3DVolumeTexture9</a>**</b>

Address of a pointer to an <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9">IDirect3DVolumeTexture9</a> interface, representing the created volume texture resource.

### -param pSharedHandle [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HANDLE</a>*</b>

Reserved. Set this parameter to <b>NULL</b>. This parameter can be used in Direct3D 9 for Windows Vista to <a href="/windows/desktop/direct3d9/dx9lh">share resources</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_INVALIDCALL, D3DERR_OUTOFVIDEOMEMORY, E_OUTOFMEMORY.

## -see-also

<a href="/windows/desktop/direct3d9/d3dxcreatevolumetexture">D3DXCreateVolumeTexture</a>



<a href="/windows/desktop/direct3d9/d3dxcreatevolumetexturefromfile">D3DXCreateVolumeTextureFromFile</a>



<a href="/windows/desktop/direct3d9/d3dxcreatevolumetexturefromfileex">D3DXCreateVolumeTextureFromFileEx</a>



<a href="/windows/desktop/direct3d9/d3dxcreatevolumetexturefromfileinmemory">D3DXCreateVolumeTextureFromFileInMemory</a>



<a href="/windows/desktop/direct3d9/d3dxcreatevolumetexturefromfileinmemoryex">D3DXCreateVolumeTextureFromFileInMemoryEx</a>



<a href="/windows/desktop/direct3d9/d3dxcreatevolumetexturefromresource">D3DXCreateVolumeTextureFromResource</a>



<a href="/windows/desktop/direct3d9/d3dxcreatevolumetexturefromresourceex">D3DXCreateVolumeTextureFromResourceEx</a>



<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>
