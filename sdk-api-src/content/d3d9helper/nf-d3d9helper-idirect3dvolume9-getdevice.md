---
UID: NF:d3d9helper.IDirect3DVolume9.GetDevice
title: IDirect3DVolume9::GetDevice
author: windows-sdk-content
description: Retrieves the device associated with a volume.
old-location: direct3d9\idirect3dvolume9__getdevice.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dvolume9__getdevice.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: 5da9af5e-dec3-9d5d-d8ca-6c45db664c38, GetDevice, GetDevice method [Direct3D 9], GetDevice method [Direct3D 9],IDirect3DVolume9 interface, IDirect3DVolume9 interface [Direct3D 9],GetDevice method, IDirect3DVolume9.GetDevice, IDirect3DVolume9::GetDevice, d3d9helper/IDirect3DVolume9::GetDevice, direct3d9.idirect3dvolume9__getdevice
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
 - IDirect3DVolume9.GetDevice
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
- IDirect3DVolume9.GetDevice
: 
---

# IDirect3DVolume9::GetDevice


## -description


Retrieves the device associated with a volume.


## -parameters




### -param ppDevice [out, retval]

Type: <b><a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a> interface to fill with the device pointer, if the query succeeds. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



This method allows navigation to the owning device object. 

Calling this method will increase the internal reference count on the <a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a> interface. Failure to call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> when finished using this <b>IDirect3DDevice9</b> interface results in a memory leak.




## -see-also




<a href="https://msdn.microsoft.com/b157d2d1-5813-43a1-ac3a-000b13b1bb62">IDirect3DVolume9</a>
 

 

