---
UID: NF:d3d9.IDirect3DDevice9.GetTexture
title: IDirect3DDevice9::GetTexture
author: windows-sdk-content
description: Retrieves a texture assigned to a stage for a device.
old-location: direct3d9\idirect3ddevice9__gettexture.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__gettexture.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: GetTexture, GetTexture method [Direct3D 9], GetTexture method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetTexture method, IDirect3DDevice9.GetTexture, IDirect3DDevice9::GetTexture, b36b5e1a-bf59-6db1-b704-5002886b044f, d3d9helper/IDirect3DDevice9::GetTexture, direct3d9.idirect3ddevice9__gettexture
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d9.h
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
req.typenames: D3D12_SIGNATURE_PARAMETER_DESC
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
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::GetTexture


## -description


Retrieves a texture assigned to a stage for a device.


## -parameters




### -param Stage [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Stage identifier of the texture to retrieve. Stage identifiers are zero-based.


### -param ppTexture [out, retval]

Type: <b><a href="https://msdn.microsoft.com/d4d7f8b9-2e7b-4445-8380-2d321a46e064">IDirect3DBaseTexture9</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/d4d7f8b9-2e7b-4445-8380-2d321a46e064">IDirect3DBaseTexture9</a> interface, representing the returned texture. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



Typically, methods that return state will not work on a device that is created using D3DCREATE_PUREDEVICE. This method however, will work even on a pure device because it returns an interface.

Calling this method will increase the internal reference count on the <a href="https://msdn.microsoft.com/fcea1048-1d9b-409f-9b5a-cdf85c30c76e">IDirect3DTexture9</a> interface. Failure to call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> when finished using this <b>IDirect3DTexture9</b> interface results in a memory leak.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/8ecc2019-16f9-4c32-9ecb-33c2b85108dc">IDirect3DDevice9::GetTextureStageState</a>



<a href="https://msdn.microsoft.com/ec62aeee-037f-4c33-b242-e0483872016c">IDirect3DDevice9::SetTexture</a>



<a href="https://msdn.microsoft.com/303f7a80-edaf-4106-a4ce-8fb7a7d30a5a">IDirect3DDevice9::SetTextureStageState</a>
 

 

