---
UID: NF:d3d11.ID3D11DeviceContext.DrawAuto
title: ID3D11DeviceContext::DrawAuto (d3d11.h)
description: Draw geometry of an unknown size.
helpviewer_keywords: ["DrawAuto","DrawAuto method [Direct3D 11]","DrawAuto method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","DrawAuto method","ID3D11DeviceContext.DrawAuto","ID3D11DeviceContext::DrawAuto","d3d11/ID3D11DeviceContext::DrawAuto","d5e26d9c-e682-ea81-70bc-d35792e62157","direct3d11.id3d11devicecontext_drawauto"]
old-location: direct3d11\id3d11devicecontext_drawauto.htm
tech.root: direct3d11
ms.assetid: 34688e87-514f-4f85-b56b-e0245400a5ac
ms.date: 12/05/2018
ms.keywords: DrawAuto, DrawAuto method [Direct3D 11], DrawAuto method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],DrawAuto method, ID3D11DeviceContext.DrawAuto, ID3D11DeviceContext::DrawAuto, d3d11/ID3D11DeviceContext::DrawAuto, d5e26d9c-e682-ea81-70bc-d35792e62157, direct3d11.id3d11devicecontext_drawauto
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11DeviceContext::DrawAuto
 - d3d11/ID3D11DeviceContext::DrawAuto
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.DrawAuto
---

# ID3D11DeviceContext::DrawAuto


## -description

Draw geometry of an unknown size.



## -remarks

A draw API submits work to the rendering pipeline. This API submits work of an unknown size that was processed by the input assembler, vertex shader, and stream-output stages;  the work may or may not have gone through the geometry-shader stage.

After data has been streamed out to stream-output stage buffers, those buffers can be again bound to the Input Assembler stage at input slot 0 and DrawAuto will draw them without the application needing to know the amount of data that was written to the buffers. A measurement of the amount of data written to the SO stage buffers is maintained internally when the data is streamed out. This means that the CPU does not need to fetch the measurement before re-binding the data that was streamed as input data. Although this amount is tracked internally, it is still the responsibility of applications to use input layouts to describe the format of the data in the SO stage buffers so that the layouts are available when the buffers are again bound to the input assembler.

The following diagram shows the DrawAuto process.

<img alt="Diagram of DrawAuto as data moves through several stages to a buffer and then back to the Input Assembler stage" src="./images/d3d11_pipeline_stages_drawauto.png"/>

Calling DrawAuto does not change the state of the streaming-output buffers that were bound again as inputs.

DrawAuto only works when drawing with one input buffer bound as an input to the IA stage at slot 0. Applications must create the SO buffer resource with both binding flags, <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_bind_flag">D3D11_BIND_VERTEX_BUFFER</a> and <b>D3D11_BIND_STREAM_OUTPUT</b>.

This API does not support indexing or instancing.

If an application needs to retrieve the size of the streaming-output buffer, it can query for statistics on streaming output by using <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_query">D3D11_QUERY_SO_STATISTICS</a>.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
