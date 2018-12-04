---
UID: NF:d3d9helper.IDirect3D9.GetDeviceCaps
title: IDirect3D9::GetDeviceCaps
author: windows-sdk-content
description: Retrieves device-specific information about a device.
old-location: direct3d9\idirect3d9__getdevicecaps.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3d9__getdevicecaps.htm
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: 87e98d3f-7bf9-d2ba-4731-1b08cb375732, GetDeviceCaps, GetDeviceCaps method [Direct3D 9], GetDeviceCaps method [Direct3D 9],IDirect3D9 interface, IDirect3D9 interface [Direct3D 9],GetDeviceCaps method, IDirect3D9.GetDeviceCaps, IDirect3D9::GetDeviceCaps, d3d9helper/IDirect3D9::GetDeviceCaps, direct3d9.idirect3d9__getdevicecaps
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
 - IDirect3D9.GetDeviceCaps
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3D9::GetDeviceCaps


## -description


Retrieves device-specific information about a device. 


## -parameters




### -param Adapter [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Ordinal number that denotes the display adapter. D3DADAPTER_DEFAULT is always the primary display adapter. 


### -param DeviceType [in]

Type: <b><a href="https://msdn.microsoft.com/2bcdc476-7c42-4152-b107-58366faf2abd">D3DDEVTYPE</a></b>

Member of the <a href="https://msdn.microsoft.com/2bcdc476-7c42-4152-b107-58366faf2abd">D3DDEVTYPE</a> enumerated type. Denotes the device type. 


### -param pCaps [out]

Type: <b><a href="https://msdn.microsoft.com/44457b7b-a1f7-4019-b971-8ec2334d3313">D3DCAPS9</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/44457b7b-a1f7-4019-b971-8ec2334d3313">D3DCAPS9</a> structure to be filled with information describing the capabilities of the device. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_INVALIDCALL, D3DERR_INVALIDDEVICE, D3DERR_OUTOFVIDEOMEMORY, and D3DERR_NOTAVAILABLE.




## -remarks



The application should not assume the persistence of vertex processing capabilities across Direct3D device objects. The particular capabilities that a physical device exposes may depend on parameters supplied to <a href="https://msdn.microsoft.com/22ad1d16-c1cc-4591-8311-daf6cf9924bb">CreateDevice</a>. For example, the capabilities may yield different vertex processing capabilities before and after creating a Direct3D Device Object with hardware vertex processing enabled. For more information see the description of <a href="https://msdn.microsoft.com/44457b7b-a1f7-4019-b971-8ec2334d3313">D3DCAPS9</a>.




## -see-also




<a href="https://msdn.microsoft.com/af321e4f-aaff-4285-bdac-9aab5c1dc5d8">IDirect3D9</a>
 

 

