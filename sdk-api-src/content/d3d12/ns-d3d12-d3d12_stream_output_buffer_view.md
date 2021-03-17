---
UID: NS:d3d12.D3D12_STREAM_OUTPUT_BUFFER_VIEW
title: D3D12_STREAM_OUTPUT_BUFFER_VIEW (d3d12.h)
description: Describes a stream output buffer.
helpviewer_keywords: ["D3D12_STREAM_OUTPUT_BUFFER_VIEW","D3D12_STREAM_OUTPUT_BUFFER_VIEW structure","d3d12/D3D12_STREAM_OUTPUT_BUFFER_VIEW","direct3d12.d3d12_stream_output_buffer_view"]
old-location: direct3d12\d3d12_stream_output_buffer_view.htm
tech.root: direct3d12
ms.assetid: EFA4FBD7-3063-4B6A-B3B1-45418C6682FC
ms.date: 12/05/2018
ms.keywords: D3D12_STREAM_OUTPUT_BUFFER_VIEW, D3D12_STREAM_OUTPUT_BUFFER_VIEW structure, d3d12/D3D12_STREAM_OUTPUT_BUFFER_VIEW, direct3d12.d3d12_stream_output_buffer_view
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
req.typenames: D3D12_STREAM_OUTPUT_BUFFER_VIEW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_STREAM_OUTPUT_BUFFER_VIEW
 - d3d12/D3D12_STREAM_OUTPUT_BUFFER_VIEW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_STREAM_OUTPUT_BUFFER_VIEW
---

# D3D12_STREAM_OUTPUT_BUFFER_VIEW structure


## -description

Describes a stream output buffer.

## -struct-fields

### -field BufferLocation

A D3D12_GPU_VIRTUAL_ADDRESS (a UINT64) that points to the stream output buffer.
            If <b>SizeInBytes</b> is 0, this member isn't used and can be any value.

### -field SizeInBytes

The size of the stream output buffer in bytes.

### -field BufferFilledSizeLocation

The location of the value of how much data has been filled into the buffer, as a D3D12_GPU_VIRTUAL_ADDRESS (a UINT64).
            This member can't be NULL; a filled size location must be supplied (which the hardware will increment as data is output).
            If <b>SizeInBytes</b> is 0, this member isn't used and can be any value.

## -remarks

Use this structure with <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets">SOSetTargets</a>.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>