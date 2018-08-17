---
UID: NF:d3d10.ID3D10Device.GSSetConstantBuffers
title: ID3D10Device::GSSetConstantBuffers
author: windows-sdk-content
description: Set the constant buffers used by the geometry shader pipeline stage.
old-location: direct3d10\id3d10device_gssetconstantbuffers.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_gssetconstantbuffers.htm
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: 4a93383e-8523-3db8-9e49-217d1cf3ff2b, GSSetConstantBuffers, GSSetConstantBuffers method [Direct3D 10], GSSetConstantBuffers method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],GSSetConstantBuffers method, ID3D10Device.GSSetConstantBuffers, ID3D10Device::GSSetConstantBuffers, d3d10/ID3D10Device::GSSetConstantBuffers, direct3d10.id3d10device_gssetconstantbuffers
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10.h
req.include-header: 
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
 - ID3D10Device.GSSetConstantBuffers
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::GSSetConstantBuffers


## -description


Set the <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">constant buffers</a> used by the <a href="https://msdn.microsoft.com/library/Bb205146(v=VS.85).aspx">geometry shader</a> pipeline stage.


## -parameters




### -param StartSlot [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Index into the device's zero-based array to begin setting constant buffers to.


### -param NumBuffers [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of buffers to set.


### -param ppConstantBuffers [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173510(v=VS.85).aspx">ID3D10Buffer</a>*</b>

Array of constant buffers (see <a href="https://msdn.microsoft.com/en-us/library/Bb173510(v=VS.85).aspx">ID3D10Buffer</a>) being given to the device.


## -returns



Returns nothing.




## -remarks



The method will not hold references to the interfaces passed in. For that reason, applications should be careful not to release interfaces currently in use by the device.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>
 

 

