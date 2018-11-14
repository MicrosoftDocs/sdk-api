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
- apiref
: 
- COM
: 
- d3d9helper.h
: 
- IDirect3DDevice9.CreateVolumeTexture
: 
---

# IDirect3DDevice9::CreateVolumeTexture


## -description


Creates a volume texture resource.


## -parameters




### -param Width [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Width of the top-level of the volume texture, in pixels. This value must be a power of two if the D3DPTEXTURECAPS_VOLUMEMAP_POW2 member of <a href="https://msdn.microsoft.com/en-us/library/Bb172513(v=VS.85).aspx">D3DCAPS9</a> is set. The pixel dimensions of subsequent levels will be the truncated value of half of the previous level's pixel dimension (independently). Each dimension clamps at a size of 1 pixel. Thus, if the division by two results in 0 (zero), 1 will be taken instead. The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in <b>D3DCAPS9</b>.


### -param Height [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Height of the top-level of the volume texture, in pixels. This value must be a power of two if the D3DPTEXTURECAPS_VOLUMEMAP_POW2 member of <a href="https://msdn.microsoft.com/en-us/library/Bb172513(v=VS.85).aspx">D3DCAPS9</a> is set. The pixel dimensions of subsequent levels will be the truncated value of half of the previous level's pixel dimension (independently). Each dimension clamps at a size of 1 pixel. Thus, if the division by 2 results in 0 (zero), 1 will be taken instead. The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in <b>D3DCAPS9</b>.


### -param Depth [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Depth of the top-level of the volume texture, in pixels. This value must be a power of two if the D3DPTEXTURECAPS_VOLUMEMAP_POW2 member of <a href="https://msdn.microsoft.com/en-us/library/Bb172513(v=VS.85).aspx">D3DCAPS9</a> is set. The pixel dimensions of subsequent levels will be the truncated value of half of the previous level's pixel dimension (independently). Each dimension clamps at a size of 1 pixel. Thus, if the division by 2 results in 0 (zero), 1 will be taken instead. The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in <b>D3DCAPS9</b>.


### -param Levels [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of levels in the texture. If this is zero, Direct3D will generate all texture sublevels down to 1x1 pixels for hardware that supports mipmapped volume textures. Call <a href="https://msdn.microsoft.com/en-us/library/Bb174325(v=VS.85).aspx">IDirect3DBaseTexture9::GetLevelCount</a> to see the number of levels generated. 


### -param Usage [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Usage can be 0, which indicates no usage value. If usage is desired, use D3DUSAGE_DYNAMIC or D3DUSAGE_SOFTWAREPROCESSING. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Bb172625(v=VS.85).aspx">D3DUSAGE</a>. 


### -param Format [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172558(v=VS.85).aspx">D3DFORMAT</a></b>

Member of the <a href="https://msdn.microsoft.com/en-us/library/Bb172558(v=VS.85).aspx">D3DFORMAT</a> enumerated type, describing the format of all levels in the volume texture. 


### -param Pool [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172584(v=VS.85).aspx">D3DPOOL</a></b>

Member of the <a href="https://msdn.microsoft.com/en-us/library/Bb172584(v=VS.85).aspx">D3DPOOL</a> enumerated type, describing the memory class into which the volume texture should be placed. 


### -param ppVolumeTexture [out, retval]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb205941(v=VS.85).aspx">IDirect3DVolumeTexture9</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/en-us/library/Bb205941(v=VS.85).aspx">IDirect3DVolumeTexture9</a> interface, representing the created volume texture resource. 


### -param pSharedHandle [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HANDLE</a>*</b>

Reserved. Set this parameter to <b>NULL</b>. This parameter can be used in Direct3D 9 for Windows Vista to <a href="https://msdn.microsoft.com/en-us/library/Bb219800(v=VS.85).aspx">share resources</a>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_INVALIDCALL, D3DERR_OUTOFVIDEOMEMORY, E_OUTOFMEMORY.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb172810(v=VS.85).aspx">D3DXCreateVolumeTexture</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb172811(v=VS.85).aspx">D3DXCreateVolumeTextureFromFile</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb172812(v=VS.85).aspx">D3DXCreateVolumeTextureFromFileEx</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb172813(v=VS.85).aspx">D3DXCreateVolumeTextureFromFileInMemory</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb172814(v=VS.85).aspx">D3DXCreateVolumeTextureFromFileInMemoryEx</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb172815(v=VS.85).aspx">D3DXCreateVolumeTextureFromResource</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb172816(v=VS.85).aspx">D3DXCreateVolumeTextureFromResourceEx</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>
 

 

