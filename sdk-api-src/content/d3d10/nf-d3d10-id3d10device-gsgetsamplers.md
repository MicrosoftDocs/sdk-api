---
UID: NF:d3d10.ID3D10Device.GSGetSamplers
title: ID3D10Device::GSGetSamplers
author: windows-sdk-content
description: Get an array of sampler states from the geometry shader pipeline stage.
old-location: direct3d10\id3d10device_gsgetsamplers.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_gsgetsamplers.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: GSGetSamplers, GSGetSamplers method [Direct3D 10], GSGetSamplers method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],GSGetSamplers method, ID3D10Device.GSGetSamplers, ID3D10Device::GSGetSamplers, d3d10/ID3D10Device::GSGetSamplers, d4899d8d-c796-58f0-bf8b-42bb650492dc, direct3d10.id3d10device_gsgetsamplers
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ID3D10Device.GSGetSamplers
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10Device::GSGetSamplers


## -description


Get an array of sampler states from the <a href="https://msdn.microsoft.com/library/Bb205146(v=VS.85).aspx">geometry shader</a> pipeline stage.


## -parameters




### -param StartSlot [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Index into the device's zero-based array to begin getting samplers from.


### -param NumSamplers [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of samplers to get from the device. Each pipeline stage has a total of 16 sampler slots available.


### -param ppSamplers [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173833(v=VS.85).aspx">ID3D10SamplerState</a>**</b>

Arry of sampler-state pointers (see <a href="https://msdn.microsoft.com/en-us/library/Bb173833(v=VS.85).aspx">ID3D10SamplerState</a>) to be returned by the device.


## -returns



Returns nothing.




## -remarks



Any returned interfaces will have their reference count incremented by one. Applications should call <a href="https://msdn.microsoft.com/en-us/library/Dd757102(v=VS.85).aspx">IUnknown::Release</a> on the returned interfaces when they are no longer needed to avoid memory leaks.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>
 

 

