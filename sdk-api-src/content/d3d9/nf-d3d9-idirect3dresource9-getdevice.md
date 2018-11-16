---
UID: NF:d3d9.IDirect3DResource9.GetDevice
title: IDirect3DResource9::GetDevice
author: windows-sdk-content
description: Retrieves the device associated with a resource.
old-location: direct3d9\idirect3dresource9__getdevice.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dresource9__getdevice.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 3bf4048b-2238-43f9-bea2-116b8dc8df09, GetDevice, GetDevice method [Direct3D 9], GetDevice method [Direct3D 9],IDirect3DResource9 interface, IDirect3DResource9 interface [Direct3D 9],GetDevice method, IDirect3DResource9.GetDevice, IDirect3DResource9::GetDevice, d3d9helper/IDirect3DResource9::GetDevice, direct3d9.idirect3dresource9__getdevice
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d9.h
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
 - IDirect3DResource9.GetDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d9.h
: 
- IDirect3DResource9.GetDevice
: 
---

# IDirect3DResource9::GetDevice


## -description


Retrieves the device associated with a resource.


## -parameters




### -param ppDevice [out, retval]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a> interface to fill with the device pointer, if the query succeeds. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



This method allows navigation to the owning device object.

Calling this method will increase the internal reference count on the <a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a> interface. Failure to call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> when finished using this <b>IDirect3DDevice9</b> interface results in a memory leak.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205878(v=VS.85).aspx">IDirect3DResource9</a>
 

 

