---
UID: NE:d3d11.D3D11_BUFFER_UAV_FLAG
title: D3D11_BUFFER_UAV_FLAG (d3d11.h)
description: Identifies unordered-access view options for a buffer resource.
helpviewer_keywords: ["5103c5e7-101e-9c1a-35cc-e3c97e30a9d5","D3D11_BUFFER_UAV_FLAG","D3D11_BUFFER_UAV_FLAG enumeration [Direct3D 11]","D3D11_BUFFER_UAV_FLAG_APPEND","D3D11_BUFFER_UAV_FLAG_COUNTER","D3D11_BUFFER_UAV_FLAG_RAW","d3d11/D3D11_BUFFER_UAV_FLAG","d3d11/D3D11_BUFFER_UAV_FLAG_APPEND","d3d11/D3D11_BUFFER_UAV_FLAG_COUNTER","d3d11/D3D11_BUFFER_UAV_FLAG_RAW","direct3d11.d3d11_buffer_uav_flag"]
old-location: direct3d11\d3d11_buffer_uav_flag.htm
tech.root: direct3d11
ms.assetid: 13cf0083-c61a-478d-94bd-00dec4cf27b7
ms.date: 12/05/2018
ms.keywords: 5103c5e7-101e-9c1a-35cc-e3c97e30a9d5, D3D11_BUFFER_UAV_FLAG, D3D11_BUFFER_UAV_FLAG enumeration [Direct3D 11], D3D11_BUFFER_UAV_FLAG_APPEND, D3D11_BUFFER_UAV_FLAG_COUNTER, D3D11_BUFFER_UAV_FLAG_RAW, d3d11/D3D11_BUFFER_UAV_FLAG, d3d11/D3D11_BUFFER_UAV_FLAG_APPEND, d3d11/D3D11_BUFFER_UAV_FLAG_COUNTER, d3d11/D3D11_BUFFER_UAV_FLAG_RAW, direct3d11.d3d11_buffer_uav_flag
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D3D11_BUFFER_UAV_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_BUFFER_UAV_FLAG
 - d3d11/D3D11_BUFFER_UAV_FLAG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_BUFFER_UAV_FLAG
---

# D3D11_BUFFER_UAV_FLAG enumeration


## -description

Identifies unordered-access view options for a buffer resource.

## -enum-fields

### -field D3D11_BUFFER_UAV_FLAG_RAW:0x1

Resource contains raw, unstructured data.  Requires the UAV format to be DXGI_FORMAT_R32_TYPELESS.
        For more info about raw viewing of buffers, see <a href="/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro">Raw Views of Buffers</a>.

### -field D3D11_BUFFER_UAV_FLAG_APPEND:0x2

Allow data to be appended to the end of the buffer.  <b>D3D11_BUFFER_UAV_FLAG_APPEND</b> flag must also be used for 
        any view that will be used as a <a href="/windows/desktop/direct3dhlsl/sm5-object-appendstructuredbuffer">AppendStructuredBuffer</a> or a <a href="/windows/desktop/direct3dhlsl/sm5-object-consumestructuredbuffer">ConsumeStructuredBuffer</a>. 
        Requires the UAV format to be DXGI_FORMAT_UNKNOWN.

### -field D3D11_BUFFER_UAV_FLAG_COUNTER:0x4

Adds a counter to the unordered-access-view buffer.  <b>D3D11_BUFFER_UAV_FLAG_COUNTER</b> can only be used on a UAV that is a 
        <a href="/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer">RWStructuredBuffer</a> and it enables the functionality needed for the <a href="/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer-incrementcounter">IncrementCounter</a> and <a href="/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer-decrementcounter">DecrementCounter</a> methods in HLSL. Requires the UAV format to be DXGI_FORMAT_UNKNOWN.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-enums">Core Enumerations</a>



<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-enums">Resource Enumerations</a>
