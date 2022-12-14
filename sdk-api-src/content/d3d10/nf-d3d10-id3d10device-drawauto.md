---
UID: NF:d3d10.ID3D10Device.DrawAuto
title: ID3D10Device::DrawAuto (d3d10.h)
description: Draw geometry of an unknown size that was created by the geometry shader stage. See remarks.
helpviewer_keywords: ["8ce13c14-3a43-9492-8641-4e2c8d9cc273","DrawAuto","DrawAuto method [Direct3D 10]","DrawAuto method [Direct3D 10]","ID3D10Device interface","ID3D10Device interface [Direct3D 10]","DrawAuto method","ID3D10Device.DrawAuto","ID3D10Device::DrawAuto","d3d10/ID3D10Device::DrawAuto","direct3d10.id3d10device_drawauto"]
old-location: direct3d10\id3d10device_drawauto.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_drawauto.htm
ms.date: 12/05/2018
ms.keywords: 8ce13c14-3a43-9492-8641-4e2c8d9cc273, DrawAuto, DrawAuto method [Direct3D 10], DrawAuto method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],DrawAuto method, ID3D10Device.DrawAuto, ID3D10Device::DrawAuto, d3d10/ID3D10Device::DrawAuto, direct3d10.id3d10device_drawauto
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
 - ID3D10Device::DrawAuto
 - d3d10/ID3D10Device::DrawAuto
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
 - ID3D10Device.DrawAuto
---

# ID3D10Device::DrawAuto


## -description

Draw geometry of an unknown size that was created by the geometry shader stage. See remarks.



## -remarks

A <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-getting-started">draw API</a> submits work to the rendering pipeline.

After data has been streamed out to <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage">SO stage</a> buffers, those buffers can be again bound to the Input Assembler stage at input slot 0 and DrawAuto will draw them without the application needing to know the amount of data that was written to the buffers. A measurement of the amount of data written to the SO stage buffers is maintained internally when the data is streamed out. This means that the CPU does not need to fetch the measurement before re-binding the data that was streamed as input data. Although this amount is tracked internally, it is still the responsibility of applications to use input layouts to describe the format of the data in the SO stage buffers so that the layouts are available when the buffers are again bound to the input assembler.

The following diagram shows the DrawAuto process.

<img alt="Diagram of DrawAuto as data moves through several stages to a buffer and then back to the Input Assembler stage" src="./images/d3d10_pipeline_stages_drawauto.png"/>

Calling DrawAuto does not change the state of the streaming-output buffers that were bound again as inputs.

DrawAuto only works when drawing with one input buffer bound as an input to the IA stage at slot 0. Applications must create the SO buffer resource with both binding flags, <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag">D3D10_BIND_VERTEX_BUFFER</a> and <b>D3D10_BIND_STREAM_OUTPUT</b>.

This API does not support indexing or instancing.

If an application needs to retrieve the size of the streaming-output buffer, it can query for statistics on streaming output by using <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_query">D3D10_QUERY_SO_STATISTICS</a>.

Example of using DrawAuto can be found in the <a href="https://msdn.microsoft.com/library/Ee416421(v=VS.85).aspx">ParticlesGS Sample</a> and <a href="https://msdn.microsoft.com/library/Ee416423(v=VS.85).aspx">PipesGS Sample</a>.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
