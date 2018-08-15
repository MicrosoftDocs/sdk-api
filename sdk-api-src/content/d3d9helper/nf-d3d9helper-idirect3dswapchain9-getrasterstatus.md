---
UID: NF:d3d9helper.IDirect3DSwapChain9.GetRasterStatus
title: IDirect3DSwapChain9::GetRasterStatus
author: windows-sdk-content
description: Returns information describing the raster of the monitor on which the swap chain is presented.
old-location: direct3d9\idirect3dswapchain9__getrasterstatus.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dswapchain9__getrasterstatus.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 4aff9086-c86f-2455-7c76-8c5de15bd4bd, GetRasterStatus, GetRasterStatus method [Direct3D 9], GetRasterStatus method [Direct3D 9],IDirect3DSwapChain9 interface, IDirect3DSwapChain9 interface [Direct3D 9],GetRasterStatus method, IDirect3DSwapChain9.GetRasterStatus, IDirect3DSwapChain9::GetRasterStatus, d3d9helper/IDirect3DSwapChain9::GetRasterStatus, direct3d9.idirect3dswapchain9__getrasterstatus
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d9helper.h
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
req.typenames: D3DVSHADERCAPS2_0
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DSwapChain9.GetRasterStatus
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DSwapChain9::GetRasterStatus


## -description


Returns information describing the raster of the monitor on which the swap chain is presented.


## -parameters




### -param pRasterStatus [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172596(v=VS.85).aspx">D3DRASTER_STATUS</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb172596(v=VS.85).aspx">D3DRASTER_STATUS</a> structure filled with information about the position or other status of the raster on the monitor driven by this adapter. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. D3DERR_INVALIDCALL is returned if pRasterStatus is invalid or if the device does not support reading the current scan line. To determine if the device supports reading the scan line, check for the D3DCAPS_READ_SCANLINE flag in the Caps member of <a href="https://msdn.microsoft.com/en-us/library/Bb172513(v=VS.85).aspx">D3DCAPS9</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb172596(v=VS.85).aspx">D3DRASTER_STATUS</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb205899(v=VS.85).aspx">IDirect3DSwapChain9</a>
 

 

