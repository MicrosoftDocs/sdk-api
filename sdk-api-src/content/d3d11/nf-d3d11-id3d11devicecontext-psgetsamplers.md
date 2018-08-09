---
UID: NF:d3d11.ID3D11DeviceContext.PSGetSamplers
title: ID3D11DeviceContext::PSGetSamplers
author: windows-sdk-content
description: Get an array of sampler states from the pixel shader pipeline stage.
old-location: direct3d11\id3d11devicecontext_psgetsamplers.htm
old-project: direct3d11
ms.assetid: 8a86f6c8-4095-48d5-a3aa-a3eef9f4b3e8
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ID3D11DeviceContext interface [Direct3D 11],PSGetSamplers method, ID3D11DeviceContext.PSGetSamplers, ID3D11DeviceContext::PSGetSamplers, PSGetSamplers, PSGetSamplers method [Direct3D 11], PSGetSamplers method [Direct3D 11],ID3D11DeviceContext interface, d3d11/ID3D11DeviceContext::PSGetSamplers, direct3d11.id3d11devicecontext_psgetsamplers, ffce57e5-f18e-d0e2-8fb6-4ee3acfcbb90
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d11.h
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
tech.root: 
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.PSGetSamplers
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11DeviceContext::PSGetSamplers


## -description


Get an array of sampler states from the pixel shader pipeline stage.


## -parameters




### -param StartSlot [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index into a zero-based array to begin getting samplers from (ranges from 0 to D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT - 1).


### -param NumSamplers [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of samplers to get from a device context. Each pipeline stage has a total of 16 sampler slots available (ranges from 0 to D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT - StartSlot).


### -param ppSamplers [out, optional]

Type: <b><a href="https://msdn.microsoft.com/8dc2facc-4f51-4064-aab4-028a06b9d7e6">ID3D11SamplerState</a>**</b>

Arry of sampler-state interface pointers (see <a href="https://msdn.microsoft.com/8dc2facc-4f51-4064-aab4-028a06b9d7e6">ID3D11SamplerState</a>) to be returned by the device.


## -returns



Returns nothing.




## -remarks



Any returned interfaces will have their reference count incremented by one. Applications should call IUnknown::Release on the returned interfaces when they are no longer needed to avoid memory leaks.




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

