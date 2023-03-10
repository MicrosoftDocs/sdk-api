---
UID: NS:d3d12.D3D12_STREAM_OUTPUT_DESC
title: D3D12_STREAM_OUTPUT_DESC (d3d12.h)
description: Describes a streaming output buffer.
helpviewer_keywords: ["D3D12_STREAM_OUTPUT_DESC","D3D12_STREAM_OUTPUT_DESC structure","d3d12/D3D12_STREAM_OUTPUT_DESC","direct3d12.d3d12_stream_output_desc"]
old-location: direct3d12\d3d12_stream_output_desc.htm
tech.root: direct3d12
ms.assetid: 9EFAA901-857B-40E3-B4B7-7C04D53BCA67
ms.date: 12/05/2018
ms.keywords: D3D12_STREAM_OUTPUT_DESC, D3D12_STREAM_OUTPUT_DESC structure, d3d12/D3D12_STREAM_OUTPUT_DESC, direct3d12.d3d12_stream_output_desc
req.header: d3d12.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D3D12_STREAM_OUTPUT_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_STREAM_OUTPUT_DESC
 - d3d12/D3D12_STREAM_OUTPUT_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_STREAM_OUTPUT_DESC
---

# D3D12_STREAM_OUTPUT_DESC structure


## -description

Describes a streaming output buffer.

## -struct-fields

### -field pSODeclaration

An array of <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_so_declaration_entry">D3D12_SO_DECLARATION_ENTRY</a> structures. Can't be <b>NULL</b> if <b>NumEntries</b> &gt; 0.

### -field NumEntries

The number of entries in the stream output declaration array that the <b>pSODeclaration</b> member points to.

### -field pBufferStrides

An array of buffer strides; each stride is the size of an element for that buffer.

### -field NumStrides

The number of strides (or buffers) that the <b>pBufferStrides</b> member points to.

### -field RasterizedStream

The index number of the stream to be sent to the rasterizer stage.

## -remarks

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc">D3D12_GRAPHICS_PIPELINE_STATE_DESC</a> object contains a <b>D3D12_STREAM_OUTPUT_DESC</b> structure.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>