---
UID: NF:d3d9.IDirect3DDevice9.GetAvailableTextureMem
title: IDirect3DDevice9::GetAvailableTextureMem
author: windows-sdk-content
description: Returns an estimate of the amount of available texture memory.
old-location: direct3d9\idirect3ddevice9__getavailabletexturemem.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getavailabletexturemem.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 4c038892-740b-67d5-cbdf-79de3acfb3d1, GetAvailableTextureMem, GetAvailableTextureMem method [Direct3D 9], GetAvailableTextureMem method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetAvailableTextureMem method, IDirect3DDevice9.GetAvailableTextureMem, IDirect3DDevice9::GetAvailableTextureMem, d3d9helper/IDirect3DDevice9::GetAvailableTextureMem, direct3d9.idirect3ddevice9__getavailabletexturemem
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
 - IDirect3DDevice9.GetAvailableTextureMem
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
- IDirect3DDevice9.GetAvailableTextureMem
: 
---

# IDirect3DDevice9::GetAvailableTextureMem


## -description


Returns an estimate of the amount of available texture memory.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The function returns an estimate of the available texture memory.




## -remarks



The returned value is rounded to the nearest MB. This is done to reflect the fact that video memory estimates are never precise due to alignment and other issues that affect consumption by certain resources. Applications can use this value to make gross estimates of memory availability to make large-scale resource decisions such as how many levels of a mipmap to attempt to allocate, but applications cannot use this value to make small-scale decisions such as if there is enough memory left to allocate another resource.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>
 

 

