---
UID: NF:d3d10.ID3D10Device.SOSetTargets
title: ID3D10Device::SOSetTargets
author: windows-sdk-content
description: Set the target output buffers for the StreamOutput stage, which enables/disables the pipeline to stream-out data.
old-location: direct3d10\id3d10device_sosettargets.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_sosettargets.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ID3D10Device interface [Direct3D 10],SOSetTargets method, ID3D10Device.SOSetTargets, ID3D10Device::SOSetTargets, SOSetTargets, SOSetTargets method [Direct3D 10], SOSetTargets method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::SOSetTargets, direct3d10.id3d10device_sosettargets, ff1f3d28-095a-2fa4-65ed-d7fd2370cc17
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
 - ID3D10Device.SOSetTargets
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
- ID3D10Device.SOSetTargets
: 
---

# ID3D10Device::SOSetTargets


## -description


Set the target output <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">buffers</a> for the <a href="https://msdn.microsoft.com/f902dc93-9612-481b-a6bd-073e924a4c79">StreamOutput</a> stage, which enables/disables the pipeline to stream-out data.


## -parameters




### -param NumBuffers [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of buffer to bind to the device. A maximum of four output buffers can be set. If less than four are defined by the call, the remaining buffer slots are set to <b>NULL</b>. See Remarks.


### -param ppSOTargets [in]

Type: <b><a href="https://msdn.microsoft.com/a81e0dfc-9be4-4ba6-a388-9c9bb97a0fa9">ID3D10Buffer</a>*</b>

The array of output buffers (see <a href="https://msdn.microsoft.com/a81e0dfc-9be4-4ba6-a388-9c9bb97a0fa9">ID3D10Buffer</a>) to bind to the device. The buffers must have been created with the <a href="https://msdn.microsoft.com/3bbefc3b-ad05-499b-bbec-f370bf08a7f4">D3D10_BIND_STREAM_OUTPUT</a> flag.


### -param pOffsets [in]

Type: <b>const <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

Array of offsets to the output buffers from <i>ppSOTargets</i>, one offset for each buffer. The offset values must be in bytes.


## -returns



Returns nothing.




## -remarks



Call <b>ID3D10Device::SOSetTargets</b> (before any draw calls) to stream data out; call SOSetTargets with <b>NULL</b> to stop streaming data out. For an example, see Exercise 01 from the GDC 2007 workshop, which sets the stream output rendertargets before calling draw methods in the RenderInstanceToStream function.

An offset of -1 will cause the stream output buffer to be appended, continuing after the last location written to the buffer in a previous stream output pass.

Calling this method using a buffer that is currently bound for writing will effectively bind <b>NULL</b> instead because a buffer cannot be bound as both an input and an output at the same time.

The <a href="https://msdn.microsoft.com/19c81383-6ac7-49ea-98a3-bf761a32ab40">Debug Layer</a> will generate a warning whenever a resource is prevented from being bound simultaneously as an input and an output, but this will not prevent invalid data from being used by the runtime.

The method will not hold a reference to the interfaces passed in. For that reason, applications should be careful not to release an interface currently in use by the device.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

