---
UID: NF:d3d9helper.IDirect3DDevice9.CreateVolumeTexture
title: IDirect3DDevice9::CreateVolumeTexture
author: windows-sdk-content
description: Creates a volume texture resource.
old-location: direct3d9\idirect3ddevice9__createvolumetexture.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__createvolumetexture.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: CreateVolumeTexture, CreateVolumeTexture method [Direct3D 9], CreateVolumeTexture method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],CreateVolumeTexture method, IDirect3DDevice9.CreateVolumeTexture, IDirect3DDevice9::CreateVolumeTexture, d27be66d-3b8c-f3af-34b8-9478b75f7b15, d3d9helper/IDirect3DDevice9::CreateVolumeTexture, direct3d9.idirect3ddevice9__createvolumetexture
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
 - IDirect3DDevice9.CreateVolumeTexture
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDevice9::CreateVolumeTexture


## -description


Creates a volume texture resource.


## -parameters




### -param Width [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Width of the top-level of the volume texture, in pixels. This value must be a power of two if the D3DPTEXTURECAPS_VOLUMEMAP_POW2 member of <a href="https://msdn.microsoft.com/44457b7b-a1f7-4019-b971-8ec2334d3313">D3DCAPS9</a> is set. The pixel dimensions of subsequent levels will be the truncated value of half of the previous level's pixel dimension (independently). Each dimension clamps at a size of 1 pixel. Thus, if the division by two results in 0 (zero), 1 will be taken instead. The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in <b>D3DCAPS9</b>.


### -param Height [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Height of the top-level of the volume texture, in pixels. This value must be a power of two if the D3DPTEXTURECAPS_VOLUMEMAP_POW2 member of <a href="https://msdn.microsoft.com/44457b7b-a1f7-4019-b971-8ec2334d3313">D3DCAPS9</a> is set. The pixel dimensions of subsequent levels will be the truncated value of half of the previous level's pixel dimension (independently). Each dimension clamps at a size of 1 pixel. Thus, if the division by 2 results in 0 (zero), 1 will be taken instead. The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in <b>D3DCAPS9</b>.


### -param Depth [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Depth of the top-level of the volume texture, in pixels. This value must be a power of two if the D3DPTEXTURECAPS_VOLUMEMAP_POW2 member of <a href="https://msdn.microsoft.com/44457b7b-a1f7-4019-b971-8ec2334d3313">D3DCAPS9</a> is set. The pixel dimensions of subsequent levels will be the truncated value of half of the previous level's pixel dimension (independently). Each dimension clamps at a size of 1 pixel. Thus, if the division by 2 results in 0 (zero), 1 will be taken instead. The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in <b>D3DCAPS9</b>.


### -param Levels [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of levels in the texture. If this is zero, Direct3D will generate all texture sublevels down to 1x1 pixels for hardware that supports mipmapped volume textures. Call <a href="https://msdn.microsoft.com/2174bc73-c888-4856-bb4b-ce4b9b6c581d">IDirect3DBaseTexture9::GetLevelCount</a> to see the number of levels generated. 


### -param Usage [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Usage can be 0, which indicates no usage value. If usage is desired, use D3DUSAGE_DYNAMIC or D3DUSAGE_SOFTWAREPROCESSING. For more information, see <a href="https://msdn.microsoft.com/c8823c39-8f17-441c-a42b-de3d7ec02f75">D3DUSAGE</a>. 


### -param Format [in]

Type: <b><a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a></b>

Member of the <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a> enumerated type, describing the format of all levels in the volume texture. 


### -param Pool [in]

Type: <b><a href="https://msdn.microsoft.com/29720b5f-16d7-4bd9-a7bd-e4dbfb00070b">D3DPOOL</a></b>

Member of the <a href="https://msdn.microsoft.com/29720b5f-16d7-4bd9-a7bd-e4dbfb00070b">D3DPOOL</a> enumerated type, describing the memory class into which the volume texture should be placed. 


### -param ppVolumeTexture [out, retval]

Type: <b><a href="https://msdn.microsoft.com/c92cabb8-61d1-4dcf-acf1-fddd3e007d47">IDirect3DVolumeTexture9</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/c92cabb8-61d1-4dcf-acf1-fddd3e007d47">IDirect3DVolumeTexture9</a> interface, representing the created volume texture resource. 


### -param pSharedHandle [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HANDLE</a>*</b>

Reserved. Set this parameter to <b>NULL</b>. This parameter can be used in Direct3D 9 for Windows Vista to <a href="https://msdn.microsoft.com/3cc0b08c-e126-4f1b-b5d1-0d6c1ebeb0c5">share resources</a>.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_INVALIDCALL, D3DERR_OUTOFVIDEOMEMORY, E_OUTOFMEMORY.




## -see-also




<a href="https://msdn.microsoft.com/8fc515cd-2fb3-40c7-8192-a41d93ac1e99">D3DXCreateVolumeTexture</a>



<a href="https://msdn.microsoft.com/e68ac4bb-a89a-41a1-b2ba-40a1ac519e3d">D3DXCreateVolumeTextureFromFile</a>



<a href="https://msdn.microsoft.com/fa11706a-83cc-4795-957d-6d0e1faf2a8f">D3DXCreateVolumeTextureFromFileEx</a>



<a href="https://msdn.microsoft.com/8ea22209-6110-4bef-a0d6-667f59017adc">D3DXCreateVolumeTextureFromFileInMemory</a>



<a href="https://msdn.microsoft.com/1a43f906-1826-40a3-a7a9-a0536c977164">D3DXCreateVolumeTextureFromFileInMemoryEx</a>



<a href="https://msdn.microsoft.com/82a0b7aa-69fa-450d-b0d2-769f05fd75ea">D3DXCreateVolumeTextureFromResource</a>



<a href="https://msdn.microsoft.com/02f2cb9e-4750-4854-aa74-202426427af5">D3DXCreateVolumeTextureFromResourceEx</a>



<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>
 

 

