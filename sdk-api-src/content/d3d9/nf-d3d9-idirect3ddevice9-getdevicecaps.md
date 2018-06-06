---
UID: NF:d3d9.IDirect3DDevice9.GetDeviceCaps
title: IDirect3DDevice9::GetDeviceCaps
author: windows-sdk-content
description: Retrieves the capabilities of the rendering device.
old-location: direct3d9\idirect3ddevice9__getdevicecaps.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getdevicecaps.htm
ms.author: windowssdkdev
ms.date: 04/10/2018
ms.keywords: 1ca27ef9-f4c4-dcea-6966-4bbfcf987b8e, GetDeviceCaps, GetDeviceCaps method [Direct3D 9], GetDeviceCaps method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetDeviceCaps method, IDirect3DDevice9.GetDeviceCaps, IDirect3DDevice9::GetDeviceCaps, d3d9helper/IDirect3DDevice9::GetDeviceCaps, direct3d9.idirect3ddevice9__getdevicecaps
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DDevice9.GetDeviceCaps
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::GetDeviceCaps


## -description


Retrieves the capabilities of the rendering device.


## -parameters




### -param pCaps [out]

Type: <b><a href="https://msdn.microsoft.com/44457b7b-a1f7-4019-b971-8ec2334d3313">D3DCAPS9</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/44457b7b-a1f7-4019-b971-8ec2334d3313">D3DCAPS9</a> structure, describing the returned device. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



<b>IDirect3DDevice9::GetDeviceCaps</b> retrieves the software vertex pipeline capabilities when the device is being used in software vertex processing mode. 
    
    
    




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>
 

 

