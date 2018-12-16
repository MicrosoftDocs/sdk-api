---
UID: NF:d3d9.IDirect3D9Ex.EnumAdapterModesEx
title: IDirect3D9Ex::EnumAdapterModesEx
author: windows-sdk-content
description: This method returns the actual display mode info based on the given mode index.
old-location: direct3d9\idirect3d9ex_enumadaptermodesex.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3d9ex_enumadaptermodesex.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 4bc3b89a-9f5a-0632-2b67-102fd92c5053, EnumAdapterModesEx, EnumAdapterModesEx method [Direct3D 9], EnumAdapterModesEx method [Direct3D 9],IDirect3D9Ex interface, IDirect3D9Ex interface [Direct3D 9],EnumAdapterModesEx method, IDirect3D9Ex.EnumAdapterModesEx, IDirect3D9Ex::EnumAdapterModesEx, d3d9/IDirect3D9Ex::EnumAdapterModesEx, direct3d9.idirect3d9ex_enumadaptermodesex
ms.topic: method
req.header: d3d9.h
req.include-header: 
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
 - IDirect3D9Ex.EnumAdapterModesEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3D9Ex::EnumAdapterModesEx


## -description


This method returns the actual display mode info based on the given mode index.


## -parameters




### -param Adapter [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Ordinal number denoting the display adapter to enumerate. D3DADAPTER_DEFAULT is always the primary display adapter. This method returns D3DERR_INVALIDCALL when this value equals or exceeds the number of display adapters in the system.


### -param pFilter [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Bb172550(v=VS.85).aspx">D3DDISPLAYMODEFILTER</a>*</b>

See <a href="https://msdn.microsoft.com/en-us/library/Bb172550(v=VS.85).aspx">D3DDISPLAYMODEFILTER</a>.


### -param Mode [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Represents the display-mode index which is an unsigned integer between zero and the value returned by GetAdapterModeCount minus one.


### -param pMode [out, retval]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172549(v=VS.85).aspx">D3DDISPLAYMODEEX</a>*</b>

A pointer to the available display mode of type <a href="https://msdn.microsoft.com/en-us/library/Bb172549(v=VS.85).aspx">D3DDISPLAYMODEEX</a>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

<ul>
<li>If the device can be used on this adapter, D3D_OK is returned.</li>
<li>If the Adapter equals or exceeds the number of display adapters in the system, D3DERR_INVALIDCALL is returned.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174301(v=VS.85).aspx">IDirect3D9Ex</a>
 

 

