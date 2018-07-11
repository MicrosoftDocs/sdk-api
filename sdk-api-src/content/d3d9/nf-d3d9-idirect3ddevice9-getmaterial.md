---
UID: NF:d3d9.IDirect3DDevice9.GetMaterial
title: IDirect3DDevice9::GetMaterial
author: windows-sdk-content
description: Retrieves the current material properties for the device.
old-location: direct3d9\idirect3ddevice9__getmaterial.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getmaterial.htm
ms.author: windowssdkdev
ms.date: 04/11/2018
ms.keywords: 47d4ab4d-62cb-0012-9d9d-20e1cadba8c4, GetMaterial, GetMaterial method [Direct3D 9], GetMaterial method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetMaterial method, IDirect3DDevice9.GetMaterial, IDirect3DDevice9::GetMaterial, d3d9helper/IDirect3DDevice9::GetMaterial, direct3d9.idirect3ddevice9__getmaterial
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
 - IDirect3DDevice9.GetMaterial
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::GetMaterial


## -description


Retrieves the current material properties for the device.


## -parameters




### -param pMaterial [out]

Type: <b><a href="https://msdn.microsoft.com/943e6f6d-8091-462f-8c44-e0c27686934a">D3DMATERIAL9</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/943e6f6d-8091-462f-8c44-e0c27686934a">D3DMATERIAL9</a> structure to fill with the currently set material properties. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. D3DERR_INVALIDCALL if the pMaterial parameter is invalid.




## -remarks



This method will not return device state for a device that is created using D3DCREATE_PUREDEVICE. If you want to use this method, you must create your device with any of the other values in <a href="https://msdn.microsoft.com/91387a2d-3927-4285-a09b-9ce247e6bfdd">D3DCREATE</a>.
    





## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/52cdcd0c-1cc9-4849-91e2-822414f7f186">IDirect3DDevice9::SetMaterial</a>
 

 

