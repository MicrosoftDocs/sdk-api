---
UID: NF:d3d9.IDirect3D9.GetAdapterModeCount
title: IDirect3D9::GetAdapterModeCount
author: windows-sdk-content
description: Returns the number of display modes available on this adapter.
old-location: direct3d9\idirect3d9__getadaptermodecount.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3d9__getadaptermodecount.htm
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: 8c15b401-a18e-3d6f-8b01-fd6833879d87, GetAdapterModeCount, GetAdapterModeCount method [Direct3D 9], GetAdapterModeCount method [Direct3D 9],IDirect3D9 interface, IDirect3D9 interface [Direct3D 9],GetAdapterModeCount method, IDirect3D9.GetAdapterModeCount, IDirect3D9::GetAdapterModeCount, d3d9helper/IDirect3D9::GetAdapterModeCount, direct3d9.idirect3d9__getadaptermodecount
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
 - IDirect3D9.GetAdapterModeCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3D9::GetAdapterModeCount


## -description


Returns the number of display modes available on this adapter.


## -parameters




### -param Adapter [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Ordinal number that denotes the display adapter. D3DADAPTER_DEFAULT is always the primary display adapter. 


### -param Format [in]

Type: <b><a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a></b>

Identifies the format of the surface type using <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a>. Use <a href="https://msdn.microsoft.com/2e86d5bf-c7ac-47a8-af6c-0cd953d4cfa0">EnumAdapterModes</a> to see the valid formats.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

This method returns the number of display modes on this adapter or zero if Adapter is greater than or equal to the number of adapters on the system.




## -see-also




<a href="https://msdn.microsoft.com/2e86d5bf-c7ac-47a8-af6c-0cd953d4cfa0">EnumAdapterModes</a>



<a href="https://msdn.microsoft.com/af321e4f-aaff-4285-bdac-9aab5c1dc5d8">IDirect3D9</a>
 

 

