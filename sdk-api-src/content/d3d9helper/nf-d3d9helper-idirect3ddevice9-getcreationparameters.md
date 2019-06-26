---
UID: NF:d3d9helper.IDirect3DDevice9.GetCreationParameters
title: IDirect3DDevice9::GetCreationParameters (d3d9helper.h)
author: windows-sdk-content
description: Retrieves the creation parameters of the device.
old-location: direct3d9\idirect3ddevice9__getcreationparameters.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getcreationparameters.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 54c41207-f279-d889-1545-426a901cafd7, GetCreationParameters, GetCreationParameters method [Direct3D 9], GetCreationParameters method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetCreationParameters method, IDirect3DDevice9.GetCreationParameters, IDirect3DDevice9::GetCreationParameters, d3d9helper/IDirect3DDevice9::GetCreationParameters, direct3d9.idirect3ddevice9__getcreationparameters
ms.topic: method
f1_keywords: 
 - "d3d9helper/IDirect3DDevice9.GetCreationParameters"
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
 - IDirect3DDevice9.GetCreationParameters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirect3DDevice9::GetCreationParameters


## -description


Retrieves the creation parameters of the device.


## -parameters




### -param pParameters [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/direct3d9/d3ddevice-creation-parameters">D3DDEVICE_CREATION_PARAMETERS</a>*</b>

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/direct3d9/d3ddevice-creation-parameters">D3DDEVICE_CREATION_PARAMETERS</a> structure, describing the creation parameters of the device. 


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK.


D3DERR_INVALIDCALL is returned if the argument is invalid.




## -remarks



You can query the AdapterOrdinal member of the returned <a href="https://docs.microsoft.com/windows/desktop/direct3d9/d3ddevice-creation-parameters">D3DDEVICE_CREATION_PARAMETERS</a> structure to retrieve the ordinal of the adapter represented by this device. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>
 

 

