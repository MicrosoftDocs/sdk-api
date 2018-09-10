---
UID: NF:d3d9helper.IDirect3DCubeTexture9.GetCubeMapSurface
title: IDirect3DCubeTexture9::GetCubeMapSurface
author: windows-sdk-content
description: Retrieves a cube texture map surface.
old-location: direct3d9\idirect3dcubetexture9__getcubemapsurface.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dcubetexture9__getcubemapsurface.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: 6704f537-4e72-4fb1-e408-561e7971fd8f, GetCubeMapSurface, GetCubeMapSurface method [Direct3D 9], GetCubeMapSurface method [Direct3D 9],IDirect3DCubeTexture9 interface, IDirect3DCubeTexture9 interface [Direct3D 9],GetCubeMapSurface method, IDirect3DCubeTexture9.GetCubeMapSurface, IDirect3DCubeTexture9::GetCubeMapSurface, d3d9helper/IDirect3DCubeTexture9::GetCubeMapSurface, direct3d9.idirect3dcubetexture9__getcubemapsurface
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
 - IDirect3DCubeTexture9.GetCubeMapSurface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DCubeTexture9::GetCubeMapSurface


## -description


Retrieves a cube texture map surface.


## -parameters




### -param FaceType [in]

Type: <b><a href="https://msdn.microsoft.com/6d18b410-6f22-4202-86ae-6b3ef85e6f69">D3DCUBEMAP_FACES</a></b>

Member of the <a href="https://msdn.microsoft.com/6d18b410-6f22-4202-86ae-6b3ef85e6f69">D3DCUBEMAP_FACES</a> enumerated type, identifying a cube map face. 


### -param Level [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Specifies a level of a mipmapped cube texture. 


### -param ppCubeMapSurface [out]

Type: <b><a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a> interface, representing the returned cube texture map surface. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be: D3DERR_INVALIDCALL.




## -remarks



Calling this method will increase the internal reference count on the <a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a> interface. Failure to call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> when finished using this <b>IDirect3DSurface9</b> interface results in a memory leak.




## -see-also




<a href="https://msdn.microsoft.com/59e400ae-d2ec-425c-9adf-49cb5a24c808">IDirect3DCubeTexture9</a>
 

 

