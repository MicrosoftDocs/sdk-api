---
UID: NE:d3d12.D3D12_BUFFER_UAV_FLAGS
title: D3D12_BUFFER_UAV_FLAGS (d3d12.h)
description: Identifies unordered-access view options for a buffer resource.
helpviewer_keywords: ["D3D12_BUFFER_UAV_FLAGS","D3D12_BUFFER_UAV_FLAGS enumeration","D3D12_BUFFER_UAV_FLAG_NONE","D3D12_BUFFER_UAV_FLAG_RAW","d3d12/D3D12_BUFFER_UAV_FLAGS","d3d12/D3D12_BUFFER_UAV_FLAG_NONE","d3d12/D3D12_BUFFER_UAV_FLAG_RAW","direct3d12.d3d12_buffer_uav_flags"]
old-location: direct3d12\d3d12_buffer_uav_flags.htm
tech.root: direct3d12
ms.assetid: D5350B5B-4E15-4B9F-B3E0-5A3B1592ED5C
ms.date: 12/05/2018
ms.keywords: D3D12_BUFFER_UAV_FLAGS, D3D12_BUFFER_UAV_FLAGS enumeration, D3D12_BUFFER_UAV_FLAG_NONE, D3D12_BUFFER_UAV_FLAG_RAW, d3d12/D3D12_BUFFER_UAV_FLAGS, d3d12/D3D12_BUFFER_UAV_FLAG_NONE, d3d12/D3D12_BUFFER_UAV_FLAG_RAW, direct3d12.d3d12_buffer_uav_flags
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
req.typenames: D3D12_BUFFER_UAV_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_BUFFER_UAV_FLAGS
 - d3d12/D3D12_BUFFER_UAV_FLAGS
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
 - D3D12_BUFFER_UAV_FLAGS
---

# D3D12_BUFFER_UAV_FLAGS enumeration


## -description

Identifies unordered-access view options for a buffer resource.

## -enum-fields

### -field D3D12_BUFFER_UAV_FLAG_NONE:0

Indicates a default view.

### -field D3D12_BUFFER_UAV_FLAG_RAW:0x1

Resource contains raw, unstructured data.  Requires the UAV format to be <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT_R32_TYPELESS</a>.
            For more info about raw viewing of buffers, see <a href="/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro">Raw Views of Buffers</a>.

## -remarks

This enum is used in the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_uav">D3D12_BUFFER_UAV</a>  structure.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>
