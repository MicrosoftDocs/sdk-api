---
UID: NF:d3d10.ID3D10Device.SOSetTargets
title: ID3D10Device::SOSetTargets (d3d10.h)
description: Set the target output buffers for the StreamOutput stage, which enables/disables the pipeline to stream-out data.
helpviewer_keywords: ["ID3D10Device interface [Direct3D 10]","SOSetTargets method","ID3D10Device.SOSetTargets","ID3D10Device::SOSetTargets","SOSetTargets","SOSetTargets method [Direct3D 10]","SOSetTargets method [Direct3D 10]","ID3D10Device interface","d3d10/ID3D10Device::SOSetTargets","direct3d10.id3d10device_sosettargets","ff1f3d28-095a-2fa4-65ed-d7fd2370cc17"]
old-location: direct3d10\id3d10device_sosettargets.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_sosettargets.htm
ms.date: 12/05/2018
ms.keywords: ID3D10Device interface [Direct3D 10],SOSetTargets method, ID3D10Device.SOSetTargets, ID3D10Device::SOSetTargets, SOSetTargets, SOSetTargets method [Direct3D 10], SOSetTargets method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::SOSetTargets, direct3d10.id3d10device_sosettargets, ff1f3d28-095a-2fa4-65ed-d7fd2370cc17
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Device::SOSetTargets
 - d3d10/ID3D10Device::SOSetTargets
dev_langs:
 - c++
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
---

# ID3D10Device::SOSetTargets


## -description

Set the target output <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">buffers</a> for the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage">StreamOutput</a> stage, which enables/disables the pipeline to stream-out data.

## -parameters

### -param NumBuffers [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of buffer to bind to the device. A maximum of four output buffers can be set. If less than four are defined by the call, the remaining buffer slots are set to <b>NULL</b>. See Remarks.

### -param ppSOTargets [in]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10buffer">ID3D10Buffer</a>*</b>

The array of output buffers (see <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10buffer">ID3D10Buffer</a>) to bind to the device. The buffers must have been created with the <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag">D3D10_BIND_STREAM_OUTPUT</a> flag.

### -param pOffsets [in]

Type: <b>const <a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

Array of offsets to the output buffers from <i>ppSOTargets</i>, one offset for each buffer. The offset values must be in bytes.

## -remarks

Call <b>ID3D10Device::SOSetTargets</b> (before any draw calls) to stream data out; call SOSetTargets with <b>NULL</b> to stop streaming data out. For an example, see Exercise 01 from the GDC 2007 workshop, which sets the stream output rendertargets before calling draw methods in the RenderInstanceToStream function.

An offset of -1 will cause the stream output buffer to be appended, continuing after the last location written to the buffer in a previous stream output pass.

Calling this method using a buffer that is currently bound for writing will effectively bind <b>NULL</b> instead because a buffer cannot be bound as both an input and an output at the same time.

The <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-api-features-layers">Debug Layer</a> will generate a warning whenever a resource is prevented from being bound simultaneously as an input and an output, but this will not prevent invalid data from being used by the runtime.

The method will not hold a reference to the interfaces passed in. For that reason, applications should be careful not to release an interface currently in use by the device.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>