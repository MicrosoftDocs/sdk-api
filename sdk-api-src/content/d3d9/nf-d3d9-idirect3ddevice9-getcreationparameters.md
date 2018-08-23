---
UID: NF:d3d9.IDirect3DDevice9.GetCreationParameters
title: IDirect3DDevice9::GetCreationParameters
author: windows-sdk-content
description: Retrieves the creation parameters of the device.
old-location: direct3d9\idirect3ddevice9__getcreationparameters.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getcreationparameters.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: 54c41207-f279-d889-1545-426a901cafd7, GetCreationParameters, GetCreationParameters method [Direct3D 9], GetCreationParameters method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetCreationParameters method, IDirect3DDevice9.GetCreationParameters, IDirect3DDevice9::GetCreationParameters, d3d9helper/IDirect3DDevice9::GetCreationParameters, direct3d9.idirect3ddevice9__getcreationparameters
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d9.h
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
 - IDirect3DDevice9.GetCreationParameters
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::GetCreationParameters


## -description


Retrieves the creation parameters of the device.


## -parameters




### -param pParameters [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172538(v=VS.85).aspx">D3DDEVICE_CREATION_PARAMETERS</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb172538(v=VS.85).aspx">D3DDEVICE_CREATION_PARAMETERS</a> structure, describing the creation parameters of the device. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK.


D3DERR_INVALIDCALL is returned if the argument is invalid.




## -remarks



You can query the AdapterOrdinal member of the returned <a href="https://msdn.microsoft.com/en-us/library/Bb172538(v=VS.85).aspx">D3DDEVICE_CREATION_PARAMETERS</a> structure to retrieve the ordinal of the adapter represented by this device. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>
 

 

