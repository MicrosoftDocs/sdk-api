---
UID: NF:d3d9helper.IDirect3DDevice9.GetDirect3D
title: IDirect3DDevice9::GetDirect3D
author: windows-driver-content
description: Returns an interface to the instance of the Direct3D object that created the device.
old-location: direct3d9\idirect3ddevice9__getdirect3d.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getdirect3d.htm
ms.author: windowsdriverdev
ms.date: 4/10/2018
ms.keywords: 81502735-fdf2-3d9f-7157-db6ecffe07a9, GetDirect3D, GetDirect3D method [Direct3D 9], GetDirect3D method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetDirect3D method, IDirect3DDevice9.GetDirect3D, IDirect3DDevice9::GetDirect3D, d3d9helper/IDirect3DDevice9::GetDirect3D, direct3d9.idirect3ddevice9__getdirect3d
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
req.typenames: D3DVSHADERCAPS2_0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D9.lib
-	D3D9.dll
api_name:
-	IDirect3DDevice9.GetDirect3D
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::GetDirect3D


## -description


Returns an interface to the instance of the Direct3D object that created the device.


## -parameters




### -param ppD3D9 [out, retval]

Type: <b><a href="https://msdn.microsoft.com/af321e4f-aaff-4285-bdac-9aab5c1dc5d8">IDirect3D9</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/af321e4f-aaff-4285-bdac-9aab5c1dc5d8">IDirect3D9</a> interface, representing the interface of the Direct3D object that created the device. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



Calling <b>IDirect3DDevice9::GetDirect3D</b> will increase the internal reference count on the <a href="https://msdn.microsoft.com/af321e4f-aaff-4285-bdac-9aab5c1dc5d8">IDirect3D9</a> interface. Failure to call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> when finished using this <b>IDirect3D9</b> interface results in a memory leak.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>
 

 

