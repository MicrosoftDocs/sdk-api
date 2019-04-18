---
UID: NF:d3d10.ID3D10Device.PSGetSamplers
title: ID3D10Device::PSGetSamplers (d3d10.h)
author: windows-sdk-content
description: Get an array of sampler states from the pixel shader pipeline stage.
old-location: direct3d10\id3d10device_psgetsamplers.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_psgetsamplers.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 192d3ca7-55ed-f763-e7fe-8bb5eb1322a9, ID3D10Device interface [Direct3D 10],PSGetSamplers method, ID3D10Device.PSGetSamplers, ID3D10Device::PSGetSamplers, PSGetSamplers, PSGetSamplers method [Direct3D 10], PSGetSamplers method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::PSGetSamplers, direct3d10.id3d10device_psgetsamplers
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.PSGetSamplers
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10Device::PSGetSamplers


## -description


Get an array of sampler states from the <a href="https://msdn.microsoft.com/library/Bb205146(v=VS.85).aspx">pixel shader</a> pipeline stage.


## -parameters




### -param StartSlot [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index into the device's zero-based array to begin getting samplers from.


### -param NumSamplers [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of samplers to get from the device. Each pipeline stage has a total of 16 sampler slots available.


### -param ppSamplers [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173833(v=VS.85).aspx">ID3D10SamplerState</a>**</b>

Arry of sampler-state interface pointers (see <a href="https://msdn.microsoft.com/en-us/library/Bb173833(v=VS.85).aspx">ID3D10SamplerState</a>) to be returned by the device.


## -returns



Returns nothing.




## -remarks



Any returned interfaces will have their reference count incremented by one. Applications should call <a href="http://msdn.microsoft.com/en-us/library/ms682317(VS.85).aspx">IUnknown::Release</a> on the returned interfaces when they are no longer needed to avoid memory leaks.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>
 

 

