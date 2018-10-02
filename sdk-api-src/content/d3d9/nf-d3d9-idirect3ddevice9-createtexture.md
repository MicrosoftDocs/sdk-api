---
UID: NF:d3d9.IDirect3DDevice9.CreateTexture
title: IDirect3DDevice9::CreateTexture
author: windows-sdk-content
description: Creates a texture resource.
old-location: direct3d9\idirect3ddevice9__createtexture.htm
tech.root: Direct3D9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__createtexture.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 0ab6054e-eb96-2ef2-67bb-a8b5918e7fee, CreateTexture, CreateTexture method [Direct3D 9], CreateTexture method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],CreateTexture method, IDirect3DDevice9.CreateTexture, IDirect3DDevice9::CreateTexture, d3d9helper/IDirect3DDevice9::CreateTexture, direct3d9.idirect3ddevice9__createtexture
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDevice9::CreateTexture


## -description


Creates a texture resource.


## -parameters




### -param Width [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Width of the top-level of the texture, in pixels. The pixel dimensions of subsequent levels will be the truncated value of half of the previous level's 
        pixel dimension (independently). Each dimension clamps at a size of 1 pixel. Thus, if the division by 2 results in 0, 1 will be taken instead. 


### -param Height [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Height of the top-level of the texture, in pixels. The pixel dimensions of subsequent levels will be the truncated value of half of the previous level's 
        pixel dimension (independently). Each dimension clamps at a size of 1 pixel. Thus, if the division by 2 results in 0, 1 will be taken instead. 


### -param Levels [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of levels in the texture. If this is zero, Direct3D will generate all texture sublevels down to 1 by 1 pixels for hardware that supports 
        mipmapped textures. Call <a href="https://msdn.microsoft.com/2174bc73-c888-4856-bb4b-ce4b9b6c581d">IDirect3DBaseTexture9::GetLevelCount</a> to see the number of levels generated. 


### -param Usage [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Usage can be 0, which indicates no usage value. However, if usage is desired, use a combination of one or more <a href="https://msdn.microsoft.com/c8823c39-8f17-441c-a42b-de3d7ec02f75">D3DUSAGE</a> constants. It is 
        good practice to match the usage parameter with the behavior flags in <a href="https://msdn.microsoft.com/22ad1d16-c1cc-4591-8311-daf6cf9924bb">IDirect3D9::CreateDevice</a>. 


### -param Format [in]

Type: <b><a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a></b>

Member of the <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a> enumerated type, describing the format of all levels in the texture. 


### -param Pool [in]

Type: <b><a href="https://msdn.microsoft.com/29720b5f-16d7-4bd9-a7bd-e4dbfb00070b">D3DPOOL</a></b>

Member of the <a href="https://msdn.microsoft.com/29720b5f-16d7-4bd9-a7bd-e4dbfb00070b">D3DPOOL</a> enumerated type, describing the memory class into which the texture should be placed. 


### -param ppTexture [out, retval]

Type: <b><a href="https://msdn.microsoft.com/fcea1048-1d9b-409f-9b5a-cdf85c30c76e">IDirect3DTexture9</a>**</b>

Pointer to an <a href="https://msdn.microsoft.com/fcea1048-1d9b-409f-9b5a-cdf85c30c76e">IDirect3DTexture9</a> interface, representing the created texture resource. 


### -param pSharedHandle [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HANDLE</a>*</b>

Reserved. Set this parameter to <b>NULL</b>. This parameter can be used in Direct3D 9 for Windows Vista to 
        <a href="https://msdn.microsoft.com/3cc0b08c-e126-4f1b-b5d1-0d6c1ebeb0c5">share resources</a>.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_INVALIDCALL, 
      D3DERR_OUTOFVIDEOMEMORY, E_OUTOFMEMORY.




## -remarks



An application can discover support for <a href="https://msdn.microsoft.com/ae5955f9-e52a-41d7-a199-800e37a3e936">Automatic Generation of Mipmaps (Direct3D 9)</a> in a particular format by calling 
      <a href="https://msdn.microsoft.com/39115099-de14-424c-95a8-c5699f5c4c65">IDirect3D9::CheckDeviceFormat</a> with D3DUSAGE_AUTOGENMIPMAP. If <b>IDirect3D9::CheckDeviceFormat</b> returns D3DOK_NOAUTOGEN, 
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




<a href="https://msdn.microsoft.com/ea028aa9-4f37-4625-9e07-9072ec1a61d0">D3DXCreateTexture</a>



<a href="https://msdn.microsoft.com/247b0ee2-ee31-4090-b94c-41951b46675f">D3DXCreateTextureFromFile</a>



<a href="https://msdn.microsoft.com/820bbd77-98af-4051-a22e-825fa4dd87d8">D3DXCreateTextureFromFileEx</a>



<a href="https://msdn.microsoft.com/3ea811be-7db8-4436-b138-f0102389bb4d">D3DXCreateTextureFromFileInMemory</a>



<a href="https://msdn.microsoft.com/e515697c-0e24-4d96-b58a-dc4f27683021">D3DXCreateTextureFromFileInMemoryEx</a>



<a href="https://msdn.microsoft.com/7c841f21-5565-4923-a2fe-bbd618616f87">D3DXCreateTextureFromResource</a>



<a href="https://msdn.microsoft.com/6015e2fa-9deb-4e6a-a401-f10fb05f40b7">D3DXCreateTextureFromResourceEx</a>



<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>
 

 

