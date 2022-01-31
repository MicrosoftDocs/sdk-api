---
UID: NE:d3d12.D3D12_BUFFER_SRV_FLAGS
title: D3D12_BUFFER_SRV_FLAGS (d3d12.h)
description: Identifies how to view a buffer resource.
helpviewer_keywords: ["D3D12_BUFFER_SRV_FLAGS","D3D12_BUFFER_SRV_FLAGS enumeration","D3D12_BUFFER_SRV_FLAG_NONE","D3D12_BUFFER_SRV_FLAG_RAW","d3d12/D3D12_BUFFER_SRV_FLAGS","d3d12/D3D12_BUFFER_SRV_FLAG_NONE","d3d12/D3D12_BUFFER_SRV_FLAG_RAW","direct3d12.d3d12_buffer_srv_flags"]
old-location: direct3d12\d3d12_buffer_srv_flags.htm
tech.root: direct3d12
ms.assetid: 153F82A2-077A-4D42-8FC3-C3370999AF6C
ms.date: 12/05/2018
ms.keywords: D3D12_BUFFER_SRV_FLAGS, D3D12_BUFFER_SRV_FLAGS enumeration, D3D12_BUFFER_SRV_FLAG_NONE, D3D12_BUFFER_SRV_FLAG_RAW, d3d12/D3D12_BUFFER_SRV_FLAGS, d3d12/D3D12_BUFFER_SRV_FLAG_NONE, d3d12/D3D12_BUFFER_SRV_FLAG_RAW, direct3d12.d3d12_buffer_srv_flags
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
req.typenames: D3D12_BUFFER_SRV_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_BUFFER_SRV_FLAGS
 - d3d12/D3D12_BUFFER_SRV_FLAGS
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
 - D3D12_BUFFER_SRV_FLAGS
---

# D3D12_BUFFER_SRV_FLAGS enumeration


## -description

Identifies how to view a buffer resource.

## -enum-fields

### -field D3D12_BUFFER_SRV_FLAG_NONE:0

Indicates a default view.

### -field D3D12_BUFFER_SRV_FLAG_RAW:0x1

View the buffer as raw. For more info about raw viewing of buffers, see <a href="/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro">Raw Views of Buffers</a>.

## -remarks

This enumeration is used by <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_srv">D3D12_BUFFER_SRV</a>.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>
