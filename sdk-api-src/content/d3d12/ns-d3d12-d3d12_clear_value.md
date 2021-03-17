---
UID: NS:d3d12.D3D12_CLEAR_VALUE
title: D3D12_CLEAR_VALUE (d3d12.h)
description: Describes a value used to optimize clear operations for a particular resource.
helpviewer_keywords: ["D3D12_CLEAR_VALUE","D3D12_CLEAR_VALUE structure","d3d12/D3D12_CLEAR_VALUE","direct3d12.d3d12_clear_value"]
old-location: direct3d12\d3d12_clear_value.htm
tech.root: direct3d12
ms.assetid: 03B67F91-C150-4719-8C43-D04F51DC9C06
ms.date: 12/05/2018
ms.keywords: D3D12_CLEAR_VALUE, D3D12_CLEAR_VALUE structure, d3d12/D3D12_CLEAR_VALUE, direct3d12.d3d12_clear_value
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
req.typenames: D3D12_CLEAR_VALUE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_CLEAR_VALUE
 - d3d12/D3D12_CLEAR_VALUE
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
 - D3D12_CLEAR_VALUE
---

# D3D12_CLEAR_VALUE structure


## -description

Describes a value used to optimize clear operations for a particular resource.

## -struct-fields

### -field Format

Specifies one member of the <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> enum.

The format of the commonly cleared color follows the same validation rules as a view/ descriptor creation. In general, the format of the clear color can be any format in the same typeless group that the resource format belongs to.

This <i>Format</i> must match the format of the view used during the clear operation. It indicates whether the <i>Color</i> or the <i>DepthStencil</i> member is valid and how to convert the values for usage with the resource.

### -field Color

Specifies a 4-entry array of float values, determining the RGBA value. The order of RGBA matches the order used with <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview">ClearRenderTargetView</a>.

### -field DepthStencil

Specifies one member of <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_value">D3D12_DEPTH_STENCIL_VALUE</a>. These values match the semantics of <i>Depth</i> and <i>Stencil</i> in <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview">ClearDepthStencilView</a>.

## -remarks

This structure is optionally passed into the following methods:
        

<ul>
<li>
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource">ID3D12Device::CreateCommittedResource</a>
</li>
<li>
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource">ID3D12Device::CreatePlacedResource</a>
</li>
<li>
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource">ID3D12Device::CreateReservedResource</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/direct3d12/cd3dx12-clear-value">CD3DX12_CLEAR_VALUE</a>



<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>