---
UID: NF:d3d9helper.IDirect3DDevice9.GetTexture
title: IDirect3DDevice9::GetTexture
author: windows-sdk-content
description: Retrieves a texture assigned to a stage for a device.
old-location: direct3d9\idirect3ddevice9__gettexture.htm
tech.root: Direct3D9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__gettexture.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetTexture, GetTexture method [Direct3D 9], GetTexture method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetTexture method, IDirect3DDevice9.GetTexture, IDirect3DDevice9::GetTexture, b36b5e1a-bf59-6db1-b704-5002886b044f, d3d9helper/IDirect3DDevice9::GetTexture, direct3d9.idirect3ddevice9__gettexture
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
 - IDirect3DDevice9.GetTexture
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDevice9::GetTexture


## -description


Retrieves a texture assigned to a stage for a device.


## -parameters




### -param Stage [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Stage identifier of the texture to retrieve. Stage identifiers are zero-based.


### -param ppTexture [out, retval]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb174322(v=VS.85).aspx">IDirect3DBaseTexture9</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/en-us/library/Bb174322(v=VS.85).aspx">IDirect3DBaseTexture9</a> interface, representing the returned texture. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



Typically, methods that return state will not work on a device that is created using D3DCREATE_PUREDEVICE. This method however, will work even on a pure device because it returns an interface.

Calling this method will increase the internal reference count on the <a href="https://msdn.microsoft.com/en-us/library/Bb205909(v=VS.85).aspx">IDirect3DTexture9</a> interface. Failure to call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> when finished using this <b>IDirect3DTexture9</b> interface results in a memory leak.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174413(v=VS.85).aspx">IDirect3DDevice9::GetTextureStageState</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174461(v=VS.85).aspx">IDirect3DDevice9::SetTexture</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174462(v=VS.85).aspx">IDirect3DDevice9::SetTextureStageState</a>
 

 

