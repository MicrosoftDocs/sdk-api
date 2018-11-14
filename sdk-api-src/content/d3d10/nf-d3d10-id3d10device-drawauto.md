---
UID: NF:d3d10.ID3D10Device.DrawAuto
title: ID3D10Device::DrawAuto
author: windows-sdk-content
description: Draw geometry of an unknown size that was created by the geometry shader stage. See remarks.
old-location: direct3d10\id3d10device_drawauto.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_drawauto.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 8ce13c14-3a43-9492-8641-4e2c8d9cc273, DrawAuto, DrawAuto method [Direct3D 10], DrawAuto method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],DrawAuto method, ID3D10Device.DrawAuto, ID3D10Device::DrawAuto, d3d10/ID3D10Device::DrawAuto, direct3d10.id3d10device_drawauto
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
 - ID3D10Device.DrawAuto
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
- ID3D10Device.DrawAuto
: 
---

# ID3D10Device::DrawAuto


## -description


Draw geometry of an unknown size that was created by the geometry shader stage. See remarks.


## -parameters






## -returns



Returns nothing.




## -remarks



A <a href="https://msdn.microsoft.com/84c0ca29-2356-4b7f-98ee-ff1758edc540">draw API</a> submits work to the rendering pipeline.

After data has been streamed out to <a href="https://msdn.microsoft.com/f902dc93-9612-481b-a6bd-073e924a4c79">SO stage</a> buffers, those buffers can be again bound to the Input Assembler stage at input slot 0 and DrawAuto will draw them without the application needing to know the amount of data that was written to the buffers. A measurement of the amount of data written to the SO stage buffers is maintained internally when the data is streamed out. This means that the CPU does not need to fetch the measurement before re-binding the data that was streamed as input data. Although this amount is tracked internally, it is still the responsibility of applications to use input layouts to describe the format of the data in the SO stage buffers so that the layouts are available when the buffers are again bound to the input assembler.

The following diagram shows the DrawAuto process.

<img alt="Diagram of DrawAuto as data moves through several stages to a buffer and then back to the Input Assembler stage" src="./images/d3d10_pipeline_stages_drawauto.png"/>

Calling DrawAuto does not change the state of the streaming-output buffers that were bound again as inputs.

DrawAuto only works when drawing with one input buffer bound as an input to the IA stage at slot 0. Applications must create the SO buffer resource with both binding flags, <a href="https://msdn.microsoft.com/3bbefc3b-ad05-499b-bbec-f370bf08a7f4">D3D10_BIND_VERTEX_BUFFER</a> and <b>D3D10_BIND_STREAM_OUTPUT</b>.

This API does not support indexing or instancing.

If an application needs to retrieve the size of the streaming-output buffer, it can query for statistics on streaming output by using <a href="https://msdn.microsoft.com/f50197d6-48ba-498e-8c1b-9b0ae08a8782">D3D10_QUERY_SO_STATISTICS</a>.

Example of using DrawAuto can be found in the <a href="a64ea742-2d5e-999b-a2a1-47fc80a94fda">ParticlesGS Sample</a> and <a href="9d95fe06-a330-011c-d755-e0225efe0f02">PipesGS Sample</a>.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

