---
UID: NF:d3d9helper.IDirect3DVolumeTexture9.GetVolumeLevel
title: IDirect3DVolumeTexture9::GetVolumeLevel
author: windows-sdk-content
description: Retrieves the specified volume texture level.
old-location: direct3d9\idirect3dvolumetexture9__getvolumelevel.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dvolumetexture9__getvolumelevel.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 6b38df70-e8ab-b3ca-2c91-45641b4a2e90, GetVolumeLevel, GetVolumeLevel method [Direct3D 9], GetVolumeLevel method [Direct3D 9],IDirect3DVolumeTexture9 interface, IDirect3DVolumeTexture9 interface [Direct3D 9],GetVolumeLevel method, IDirect3DVolumeTexture9.GetVolumeLevel, IDirect3DVolumeTexture9::GetVolumeLevel, d3d9helper/IDirect3DVolumeTexture9::GetVolumeLevel, direct3d9.idirect3dvolumetexture9__getvolumelevel
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d9helper.h
req.include-header: D3D9.h
req.redist: 
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
tech.root: 
req.typenames: D3DVSHADERCAPS2_0
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DVolumeTexture9.GetVolumeLevel
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DVolumeTexture9::GetVolumeLevel


## -description


Retrieves the specified volume texture level.


## -parameters




### -param Level [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Identifies a level of the volume texture resource. This method returns a volume for the level specified by this parameter. 


### -param ppVolumeLevel [out, retval]

Type: <b><a href="https://msdn.microsoft.com/b157d2d1-5813-43a1-ac3a-000b13b1bb62">IDirect3DVolume9</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/b157d2d1-5813-43a1-ac3a-000b13b1bb62">IDirect3DVolume9</a> interface, representing the returned volume level. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



Calling this method will increase the internal reference count on the <a href="https://msdn.microsoft.com/b157d2d1-5813-43a1-ac3a-000b13b1bb62">IDirect3DVolume9</a> interface. Failure to call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> when finished using this <b>IDirect3DVolume9</b> interface results in a memory leak.




## -see-also




<a href="https://msdn.microsoft.com/c92cabb8-61d1-4dcf-acf1-fddd3e007d47">IDirect3DVolumeTexture9</a>
 

 

