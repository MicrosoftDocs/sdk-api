---
UID: NF:d3d9.IDirect3DDevice9.GetRasterStatus
title: IDirect3DDevice9::GetRasterStatus
author: windows-sdk-content
description: Returns information describing the raster of the monitor on which the swap chain is presented.
old-location: direct3d9\idirect3ddevice9__getrasterstatus.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getrasterstatus.htm
ms.author: windowssdkdev
ms.date: 04/10/2018
ms.keywords: GetRasterStatus, GetRasterStatus method [Direct3D 9], GetRasterStatus method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetRasterStatus method, IDirect3DDevice9.GetRasterStatus, IDirect3DDevice9::GetRasterStatus, a1fc6bf1-1e43-8a94-f293-1f38f3147f02, d3d9helper/IDirect3DDevice9::GetRasterStatus, direct3d9.idirect3ddevice9__getrasterstatus
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D12_SIGNATURE_PARAMETER_DESC
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D9.lib
-	D3D9.dll
api_name:
-	IDirect3DDevice9.GetRasterStatus
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::GetRasterStatus


## -description


Returns information describing the raster of the monitor on which the swap chain is presented.


## -parameters




### -param iSwapChain [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

An unsigned integer specifying the swap chain.


### -param pRasterStatus [out]

Type: <b><a href="https://msdn.microsoft.com/f7b5b714-8fc8-47b8-adec-1089b8d07081">D3DRASTER_STATUS</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/f7b5b714-8fc8-47b8-adec-1089b8d07081">D3DRASTER_STATUS</a> structure filled with information about the position or other status of the raster on the monitor driven by this adapter. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. D3DERR_INVALIDCALL is returned if pRasterStatus is invalid or if the device does not support reading the current scan line. To determine if the device supports reading the scan line, check for the D3DCAPS_READ_SCANLINE flag in the Caps member of <a href="https://msdn.microsoft.com/44457b7b-a1f7-4019-b971-8ec2334d3313">D3DCAPS9</a>.




## -see-also




<a href="https://msdn.microsoft.com/f7b5b714-8fc8-47b8-adec-1089b8d07081">D3DRASTER_STATUS</a>



<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>
 

 

