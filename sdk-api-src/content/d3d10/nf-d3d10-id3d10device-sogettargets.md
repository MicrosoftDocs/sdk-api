---
UID: NF:d3d10.ID3D10Device.SOGetTargets
title: ID3D10Device::SOGetTargets
author: windows-sdk-content
description: Get the target output buffers for the StreamOutput stage of the pipeline.
old-location: direct3d10\id3d10device_sogettargets.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_sogettargets.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 1b186699-d71b-b02e-0591-a512a5b0109d, ID3D10Device interface [Direct3D 10],SOGetTargets method, ID3D10Device.SOGetTargets, ID3D10Device::SOGetTargets, SOGetTargets, SOGetTargets method [Direct3D 10], SOGetTargets method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::SOGetTargets, direct3d10.id3d10device_sogettargets
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
 - ID3D10Device.SOGetTargets
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d10.h
: 
- ID3D10Device.SOGetTargets
: 
---

# ID3D10Device::SOGetTargets


## -description


Get the target output <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">buffers</a> for the <a href="https://msdn.microsoft.com/en-us/library/Bb205121(v=VS.85).aspx">StreamOutput</a> stage of the pipeline.


## -parameters




### -param NumBuffers [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of buffers to get. A maximum of four output buffers can be retrieved.


### -param ppSOTargets [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173510(v=VS.85).aspx">ID3D10Buffer</a>**</b>

An array of output buffers (see <a href="https://msdn.microsoft.com/en-us/library/Bb173510(v=VS.85).aspx">ID3D10Buffer</a>) to be retrieved from the device.


### -param pOffsets [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a>*</b>

Array of offsets to the output buffers from <i>ppSOTargets</i>, one offset for each buffer. The offset values are in bytes.


## -returns



Returns nothing.




## -remarks



Any returned interfaces will have their reference count incremented by one. Applications should call <a href="https://msdn.microsoft.com/en-us/library/Dd757102(v=VS.85).aspx">IUnknown::Release</a> on the returned interfaces when they are no longer needed to avoid memory leaks.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>
 

 

