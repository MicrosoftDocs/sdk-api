---
UID: NF:d3d9helper.IDirect3DDevice9.GetDepthStencilSurface
title: IDirect3DDevice9::GetDepthStencilSurface
author: windows-sdk-content
description: Gets the depth-stencil surface owned by the Direct3DDevice object.
old-location: direct3d9\idirect3ddevice9__getdepthstencilsurface.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getdepthstencilsurface.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: 838c2e61-ca4b-a0a4-7c79-dcedf679f8be, GetDepthStencilSurface, GetDepthStencilSurface method [Direct3D 9], GetDepthStencilSurface method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetDepthStencilSurface method, IDirect3DDevice9.GetDepthStencilSurface, IDirect3DDevice9::GetDepthStencilSurface, d3d9helper/IDirect3DDevice9::GetDepthStencilSurface, direct3d9.idirect3ddevice9__getdepthstencilsurface
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
 - IDirect3DDevice9.GetDepthStencilSurface
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
- IDirect3DDevice9.GetDepthStencilSurface
: 
---

# IDirect3DDevice9::GetDepthStencilSurface


## -description


Gets the depth-stencil surface owned by the Direct3DDevice object.


## -parameters




### -param ppZStencilSurface [out, retval]

Type: <b><a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a> interface, representing the returned depth-stencil surface. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK.If the device doesn't have a depth stencil buffer associated with it, the return value will be D3DERR_NOTFOUND. Otherwise, if the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



Calling this method will increase the internal reference count on the <a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a> interface. Failure to call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> when finished using this <b>IDirect3DSurface9</b> interface results in a memory leak.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/e0ffb4fc-6428-44b1-9f9d-88a5fa88d712">IDirect3DDevice9::SetDepthStencilSurface</a>
 

 

