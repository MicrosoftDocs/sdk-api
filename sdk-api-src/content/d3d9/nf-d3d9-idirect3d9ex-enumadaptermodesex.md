---
UID: NF:d3d9.IDirect3D9Ex.EnumAdapterModesEx
title: IDirect3D9Ex::EnumAdapterModesEx
author: windows-sdk-content
description: This method returns the actual display mode info based on the given mode index.
old-location: direct3d9\idirect3d9ex_enumadaptermodesex.htm
tech.root: Direct3D9
ms.assetid: VS|directx_sdk|~\idirect3d9ex_enumadaptermodesex.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 4bc3b89a-9f5a-0632-2b67-102fd92c5053, EnumAdapterModesEx, EnumAdapterModesEx method [Direct3D 9], EnumAdapterModesEx method [Direct3D 9],IDirect3D9Ex interface, IDirect3D9Ex interface [Direct3D 9],EnumAdapterModesEx method, IDirect3D9Ex.EnumAdapterModesEx, IDirect3D9Ex::EnumAdapterModesEx, d3d9/IDirect3D9Ex::EnumAdapterModesEx, direct3d9.idirect3d9ex_enumadaptermodesex
ms.prod: windows-hardware
ms.technology: windows-devices
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

Type: <b>const <a href="https://msdn.microsoft.com/4a03d0f0-dec5-4209-8c99-b58cc13064f5">D3DDISPLAYMODEFILTER</a>*</b>

See <a href="https://msdn.microsoft.com/4a03d0f0-dec5-4209-8c99-b58cc13064f5">D3DDISPLAYMODEFILTER</a>.


### -param Mode [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Represents the display-mode index which is an unsigned integer between zero and the value returned by GetAdapterModeCount minus one.


### -param pMode [out, retval]

Type: <b><a href="https://msdn.microsoft.com/df9d12b9-7acb-435b-9d54-0b095c871f0e">D3DDISPLAYMODEEX</a>*</b>

A pointer to the available display mode of type <a href="https://msdn.microsoft.com/df9d12b9-7acb-435b-9d54-0b095c871f0e">D3DDISPLAYMODEEX</a>.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

<ul>
<li>If the device can be used on this adapter, D3D_OK is returned.</li>
<li>If the Adapter equals or exceeds the number of display adapters in the system, D3DERR_INVALIDCALL is returned.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/68dbd2d4-0a38-47fc-ad3d-4ac209ed98a8">IDirect3D9Ex</a>
 

 

