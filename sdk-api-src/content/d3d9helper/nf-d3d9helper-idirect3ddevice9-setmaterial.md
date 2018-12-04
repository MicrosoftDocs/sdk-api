---
UID: NF:d3d9helper.IDirect3DDevice9.SetMaterial
title: IDirect3DDevice9::SetMaterial
author: windows-sdk-content
description: Sets the material properties for the device.
old-location: direct3d9\idirect3ddevice9__setmaterial.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setmaterial.htm
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IDirect3DDevice9 interface [Direct3D 9],SetMaterial method, IDirect3DDevice9.SetMaterial, IDirect3DDevice9::SetMaterial, SetMaterial, SetMaterial method [Direct3D 9], SetMaterial method [Direct3D 9],IDirect3DDevice9 interface, a65e098b-14ec-df07-e795-b22f5ac8fcbd, d3d9helper/IDirect3DDevice9::SetMaterial, direct3d9.idirect3ddevice9__setmaterial
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
 - IDirect3DDevice9.SetMaterial
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDevice9::SetMaterial


## -description


Sets the material properties for the device.


## -parameters




### -param pMaterial [in]

Type: <b>const <a href="https://msdn.microsoft.com/943e6f6d-8091-462f-8c44-e0c27686934a">D3DMATERIAL9</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/943e6f6d-8091-462f-8c44-e0c27686934a">D3DMATERIAL9</a> structure, describing the material properties to set. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. D3DERR_INVALIDCALL if the pMaterial parameter is invalid.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/834855f6-85ff-4c68-b1e7-8418042b71aa">IDirect3DDevice9::GetMaterial</a>
 

 

