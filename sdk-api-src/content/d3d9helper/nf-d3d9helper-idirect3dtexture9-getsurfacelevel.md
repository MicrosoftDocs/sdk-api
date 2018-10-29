---
UID: NF:d3d9helper.IDirect3DTexture9.GetSurfaceLevel
title: IDirect3DTexture9::GetSurfaceLevel
author: windows-sdk-content
description: Retrieves the specified texture surface level.
old-location: direct3d9\idirect3dtexture9__getsurfacelevel.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dtexture9__getsurfacelevel.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetSurfaceLevel, GetSurfaceLevel method [Direct3D 9], GetSurfaceLevel method [Direct3D 9],IDirect3DTexture9 interface, IDirect3DTexture9 interface [Direct3D 9],GetSurfaceLevel method, IDirect3DTexture9.GetSurfaceLevel, IDirect3DTexture9::GetSurfaceLevel, ba29c84a-8d60-aa0a-9eae-f64e0534c051, d3d9helper/IDirect3DTexture9::GetSurfaceLevel, direct3d9.idirect3dtexture9__getsurfacelevel
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
 - IDirect3DTexture9.GetSurfaceLevel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DTexture9::GetSurfaceLevel


## -description


Retrieves the specified texture surface level.


## -parameters




### -param Level [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Identifies a level of the texture resource. This method returns a surface for the level specified by this parameter. The top-level surface is denoted by 0. 


### -param ppSurfaceLevel [out, retval]

Type: <b><a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a> interface, representing the returned surface. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one D3DERR_INVALIDCALL.




## -remarks



Calling this method will increase the internal reference count on the <a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a> interface. Failure to call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> when finished using this <b>IDirect3DSurface9</b> interface results in a memory leak.




## -see-also




<a href="https://msdn.microsoft.com/fcea1048-1d9b-409f-9b5a-cdf85c30c76e">IDirect3DTexture9</a>
 

 

