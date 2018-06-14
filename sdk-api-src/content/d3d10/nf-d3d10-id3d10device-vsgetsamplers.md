---
UID: NF:d3d10.ID3D10Device.VSGetSamplers
title: ID3D10Device::VSGetSamplers
author: windows-sdk-content
description: Get an array of sampler states from the vertex shader pipeline stage.
old-location: direct3d10\id3d10device_vsgetsamplers.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_vsgetsamplers.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: 18b97598-9d43-0a9e-c706-15e272faba6b, ID3D10Device interface [Direct3D 10],VSGetSamplers method, ID3D10Device.VSGetSamplers, ID3D10Device::VSGetSamplers, VSGetSamplers, VSGetSamplers method [Direct3D 10], VSGetSamplers method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::VSGetSamplers, direct3d10.id3d10device_vsgetsamplers
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10.h
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
req.typenames: D3D10_USAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.VSGetSamplers
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::VSGetSamplers


## -description


Get an array of sampler states from the <a href="direct3d10.d3d10_graphics_programming_guide_shader_stages">vertex shader</a> pipeline stage.


## -parameters




### -param StartSlot [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index into the device's zero-based array to begin getting samplers from.


### -param NumSamplers [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of samplers to get from the device. Each pipeline stage has a total of 16 sampler slots available.


### -param ppSamplers [out]

Type: <b><a href="https://msdn.microsoft.com/5815f809-aec0-49b1-bcef-d04146551af9">ID3D10SamplerState</a>**</b>

Arry of sampler-state interface pointers (see <a href="https://msdn.microsoft.com/5815f809-aec0-49b1-bcef-d04146551af9">ID3D10SamplerState</a>) to be returned by the device.


## -returns



Returns nothing.




## -remarks



Any returned interfaces will have their reference count incremented by one. Applications should call <a href="http://msdn.microsoft.com/en-us/library/ms682317(VS.85).aspx">IUnknown::Release</a> on the returned interfaces when they are no longer needed to avoid memory leaks.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

