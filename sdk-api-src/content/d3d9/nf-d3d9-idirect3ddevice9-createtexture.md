---
UID: NF:d3d9.IDirect3DDevice9.CreateTexture
title: IDirect3DDevice9::CreateTexture (d3d9.h)
description: The IDirect3DDevice9::CreateTexture method (d3d9.h) creates a texture resource.
helpviewer_keywords: ["0ab6054e-eb96-2ef2-67bb-a8b5918e7fee","CreateTexture","CreateTexture method [Direct3D 9]","CreateTexture method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","CreateTexture method","IDirect3DDevice9.CreateTexture","IDirect3DDevice9::CreateTexture","d3d9helper/IDirect3DDevice9::CreateTexture","direct3d9.idirect3ddevice9__createtexture"]
old-location: direct3d9\idirect3ddevice9__createtexture.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__createtexture.htm
ms.date: 08/10/2022
ms.keywords: 0ab6054e-eb96-2ef2-67bb-a8b5918e7fee, CreateTexture, CreateTexture method [Direct3D 9], CreateTexture method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],CreateTexture method, IDirect3DDevice9.CreateTexture, IDirect3DDevice9::CreateTexture, d3d9helper/IDirect3DDevice9::CreateTexture, direct3d9.idirect3ddevice9__createtexture
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
 - IDirect3DDevice9::CreateTexture
 - d3d9/IDirect3DDevice9::CreateTexture
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
 - IDirect3DDevice9.CreateTexture
---

# IDirect3DDevice9::CreateTexture


## -description

Creates a texture resource.

## -parameters

### -param Width [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Width of the top-level of the texture, in pixels. The pixel dimensions of subsequent levels will be the truncated value of half of the previous level's 
        pixel dimension (independently). Each dimension clamps at a size of 1 pixel. Thus, if the division by 2 results in 0, 1 will be taken instead.

### -param Height [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Height of the top-level of the texture, in pixels. The pixel dimensions of subsequent levels will be the truncated value of half of the previous level's 
        pixel dimension (independently). Each dimension clamps at a size of 1 pixel. Thus, if the division by 2 results in 0, 1 will be taken instead.

### -param Levels [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of levels in the texture. If this is zero, Direct3D will generate all texture sublevels down to 1 by 1 pixels for hardware that supports 
        mipmapped textures. Call <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3dbasetexture9-getlevelcount">IDirect3DBaseTexture9::GetLevelCount</a> to see the number of levels generated.

### -param Usage [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Usage can be 0, which indicates no usage value. However, if usage is desired, use a combination of one or more <a href="/windows/desktop/direct3d9/d3dusage">D3DUSAGE</a> constants. It is 
        good practice to match the usage parameter with the behavior flags in <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-createdevice">IDirect3D9::CreateDevice</a>.

### -param Format [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a></b>

Member of the <a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a> enumerated type, describing the format of all levels in the texture.

### -param Pool [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dpool">D3DPOOL</a></b>

Member of the <a href="/windows/desktop/direct3d9/d3dpool">D3DPOOL</a> enumerated type, describing the memory class into which the texture should be placed.

### -param ppTexture [out, retval]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dtexture9">IDirect3DTexture9</a>**</b>

Pointer to an <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dtexture9">IDirect3DTexture9</a> interface, representing the created texture resource.

### -param pSharedHandle [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HANDLE</a>*</b>

Reserved. Set this parameter to <b>NULL</b>. This parameter can be used in Direct3D 9 for Windows Vista to 
        <a href="/windows/desktop/direct3d9/dx9lh">share resources</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_INVALIDCALL, 
      D3DERR_OUTOFVIDEOMEMORY, E_OUTOFMEMORY.

## -remarks

An application can discover support for <a href="/windows/desktop/direct3d9/automatic-generation-of-mipmaps">Automatic Generation of Mipmaps (Direct3D 9)</a> in a particular format by calling 
      <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat">IDirect3D9::CheckDeviceFormat</a> with D3DUSAGE_AUTOGENMIPMAP. If <b>IDirect3D9::CheckDeviceFormat</b> returns D3DOK_NOAUTOGEN, 
      <b>IDirect3DDevice9::CreateTexture</b> will succeed but it will return a one-level texture.

In Windows Vista CreateTexture can create a texture from a system memory pointer allowing the application more flexibility over the use, allocation and deletion of 
      the system memory.  For example, an application could pass a GDI system memory bitmap pointer and get a Direct3D texture interface around it.  Using a system memory 
      pointer with CreateTexture has the following restrictions.

<ul>
<li>The pitch of the texture must be equal to the width multiplied by the number of bytes per pixel.</li>
<li>Only textures with a single mipmap level are supported.  The <i>Levels</i> argument must be 1.</li>
<li>The <i>Pool</i> argument must be D3DPOOL_SYSTEMMEM.</li>
<li>The <i>pSharedHandle</i> argument must be a valid pointer to a buffer that can hold the system memory point; <i>*pSharedHandle</i> must 
        be a valid pointer to system memory with a size in bytes of texture width * texture height * bytes per pixel of the texture format.</li>
</ul>

## -see-also

<a href="/windows/desktop/direct3d9/d3dxcreatetexture">D3DXCreateTexture</a>



<a href="/windows/desktop/direct3d9/d3dxcreatetexturefromfile">D3DXCreateTextureFromFile</a>



<a href="/windows/desktop/direct3d9/d3dxcreatetexturefromfileex">D3DXCreateTextureFromFileEx</a>



<a href="/windows/desktop/direct3d9/d3dxcreatetexturefromfileinmemory">D3DXCreateTextureFromFileInMemory</a>



<a href="/windows/desktop/direct3d9/d3dxcreatetexturefromfileinmemoryex">D3DXCreateTextureFromFileInMemoryEx</a>



<a href="/windows/desktop/direct3d9/d3dxcreatetexturefromresource">D3DXCreateTextureFromResource</a>



<a href="/windows/desktop/direct3d9/d3dxcreatetexturefromresourceex">D3DXCreateTextureFromResourceEx</a>



<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>
