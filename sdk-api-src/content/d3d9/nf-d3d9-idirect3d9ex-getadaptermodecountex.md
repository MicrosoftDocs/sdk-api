---
UID: NF:d3d9.IDirect3D9Ex.GetAdapterModeCountEx
title: IDirect3D9Ex::GetAdapterModeCountEx
author: windows-sdk-content
description: Returns the number of display modes available.
old-location: direct3d9\idirect3d9ex_getadaptermodecountex.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3d9ex_getadaptermodecountex.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: GetAdapterModeCountEx, GetAdapterModeCountEx method [Direct3D 9], GetAdapterModeCountEx method [Direct3D 9],IDirect3D9Ex interface, IDirect3D9Ex interface [Direct3D 9],GetAdapterModeCountEx method, IDirect3D9Ex.GetAdapterModeCountEx, IDirect3D9Ex::GetAdapterModeCountEx, b588ce9d-6d83-1841-d193-8ee55c13af53, d3d9/IDirect3D9Ex::GetAdapterModeCountEx, direct3d9.idirect3d9ex_getadaptermodecountex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d9.h
req.include-header: 
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
 - IDirect3D9Ex.GetAdapterModeCountEx
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3D9Ex::GetAdapterModeCountEx


## -description


Returns the number of display modes available.


## -parameters




### -param Adapter [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Ordinal number denoting the display adapter from which to retrieve the display mode count.


### -param pFilter [in]

Type: <b>const <a href="https://msdn.microsoft.com/4a03d0f0-dec5-4209-8c99-b58cc13064f5">D3DDISPLAYMODEFILTER</a>*</b>

Specifies the characteristics of the desired display mode. See <a href="https://msdn.microsoft.com/4a03d0f0-dec5-4209-8c99-b58cc13064f5">D3DDISPLAYMODEFILTER</a>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of display modes available. A return of value zero from this method is an indication that no such display mode is supported or simply this monitor is no longer available.




## -remarks



Events such as display mode changes on other heads of the same hardware, monitor change or its connection status change, and desktop extension/unextension could all affect the number of display mode available.

To fullscreen applications, S_PRESENT_MODE_CHANGED returned from <a href="https://msdn.microsoft.com/845c72ff-669d-44bf-8065-cff456418e8c">PresentEx</a> or <a href="https://msdn.microsoft.com/89a9b112-5f0a-4e57-9b8e-48b3a76a09ce">CheckDeviceState</a> is the indication of display mode setting failure due to those events.

To increase the chance of setting a currently available display mode successfully, fullscreen applications should try to requery the available display mode list upon receiving S_PRESENT_MODE_CHANGED.




## -see-also




<a href="https://msdn.microsoft.com/68dbd2d4-0a38-47fc-ad3d-4ac209ed98a8">IDirect3D9Ex</a>
 

 

