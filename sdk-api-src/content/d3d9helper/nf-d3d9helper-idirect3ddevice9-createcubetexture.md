---
UID: NF:d3d9helper.IDirect3DDevice9.CreateCubeTexture
title: IDirect3DDevice9::CreateCubeTexture
author: windows-sdk-content
description: Creates a cube texture resource.
old-location: direct3d9\idirect3ddevice9__createcubetexture.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__createcubetexture.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: 0b1afd24-65fb-4a7c-77ef-c3b832e6d5f1, CreateCubeTexture, CreateCubeTexture method [Direct3D 9], CreateCubeTexture method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],CreateCubeTexture method, IDirect3DDevice9.CreateCubeTexture, IDirect3DDevice9::CreateCubeTexture, d3d9helper/IDirect3DDevice9::CreateCubeTexture, direct3d9.idirect3ddevice9__createcubetexture
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDevice9::CreateCubeTexture


## -description


Creates a cube texture resource.


## -parameters




### -param EdgeLength [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Size of the edges of all the top-level faces of the cube texture. The pixel dimensions of subsequent levels of each face will be the truncated value of half of the previous level's pixel dimension (independently). Each dimension clamps at a size of 1 pixel. Thus, if the division by 2 results in 0 (zero), 1 will be taken instead. 


### -param Levels [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of levels in each face of the cube texture. If this is zero, Direct3D will generate all cube texture sublevels down to 1x1 pixels for each face for hardware that supports mipmapped cube textures.  Call <a href="https://msdn.microsoft.com/2174bc73-c888-4856-bb4b-ce4b9b6c581d">IDirect3DBaseTexture9::GetLevelCount</a> to see the number of levels generated. 


### -param Usage [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Usage can be 0, which indicates no usage value. However, if usage is desired, use a combination of one or more <a href="https://msdn.microsoft.com/c8823c39-8f17-441c-a42b-de3d7ec02f75">D3DUSAGE</a> constants. It is good practice to match the usage parameter in CreateCubeTexture with the behavior flags in <a href="https://msdn.microsoft.com/22ad1d16-c1cc-4591-8311-daf6cf9924bb">IDirect3D9::CreateDevice</a>. For more information, see Remarks. 


### -param Format [in]

Type: <b><a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a></b>

Member of the <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a> enumerated type, describing the format of all levels in all faces of the cube texture. 


### -param Pool [in]

Type: <b><a href="https://msdn.microsoft.com/29720b5f-16d7-4bd9-a7bd-e4dbfb00070b">D3DPOOL</a></b>

Member of the <a href="https://msdn.microsoft.com/29720b5f-16d7-4bd9-a7bd-e4dbfb00070b">D3DPOOL</a> enumerated type, describing the memory class into which the cube texture should be placed. 


### -param ppCubeTexture [out, retval]

Type: <b><a href="https://msdn.microsoft.com/59e400ae-d2ec-425c-9adf-49cb5a24c808">IDirect3DCubeTexture9</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/59e400ae-d2ec-425c-9adf-49cb5a24c808">IDirect3DCubeTexture9</a> interface, representing the created cube texture resource. 


### -param pSharedHandle [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HANDLE</a>*</b>

Reserved. Set this parameter to <b>NULL</b>. This parameter can be used in Direct3D 9 for Windows Vista to <a href="https://msdn.microsoft.com/3cc0b08c-e126-4f1b-b5d1-0d6c1ebeb0c5">share resources</a>.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_INVALIDCALL, D3DERR_OUTOFVIDEOMEMORY, E_OUTOFMEMORY.




## -remarks



A mipmap (texture) is a collection of successively downsampled (mipmapped) surfaces. On the other hand, a cube texture (created by <b>IDirect3DDevice9::CreateCubeTexture</b>) is a collection of six textures (mipmaps), one for each face. All faces must be present in the cube texture. Also, a cube map surface must be the same pixel size in all three dimensions (x, y, and z).

An application can discover support for <a href="https://msdn.microsoft.com/ae5955f9-e52a-41d7-a199-800e37a3e936">Automatic Generation of Mipmaps (Direct3D 9)</a> in a particular format by calling <a href="https://msdn.microsoft.com/39115099-de14-424c-95a8-c5699f5c4c65">IDirect3D9::CheckDeviceFormat</a> with D3DUSAGE_AUTOGENMIPMAP. If <b>IDirect3D9::CheckDeviceFormat</b> returns D3DOK_NOAUTOGEN, <b>IDirect3DDevice9::CreateCubeTexture</b> will succeed but it will return a one-level texture.




## -see-also




<a href="https://msdn.microsoft.com/96cf3fc1-9efc-4b97-a082-2956386145c7">D3DXCreateCubeTexture</a>



<a href="https://msdn.microsoft.com/7ff3b051-568c-4c77-b8a6-b626ba156eb1">D3DXCreateCubeTextureFromFile</a>



<a href="https://msdn.microsoft.com/77e64b33-9282-42fa-978c-a93fa9ba11fc">D3DXCreateCubeTextureFromFileEx</a>



<a href="https://msdn.microsoft.com/f7e99d5a-5479-4f0b-b040-bb07e7e37666">D3DXCreateCubeTextureFromFileInMemory</a>



<a href="https://msdn.microsoft.com/598016eb-9ea9-4dca-a297-5708a957da6a">D3DXCreateCubeTextureFromFileInMemoryEx</a>



<a href="https://msdn.microsoft.com/9153944a-af8b-4365-9e91-fc1136a84caa">D3DXCreateCubeTextureFromResource</a>



<a href="https://msdn.microsoft.com/4d263386-8270-4967-8ef5-e9ac69e502a5">D3DXCreateCubeTextureFromResourceEx</a>



<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>
 

 

