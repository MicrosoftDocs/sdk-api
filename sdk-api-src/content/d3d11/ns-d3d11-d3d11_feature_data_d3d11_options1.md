---
UID: NS:d3d11.D3D11_FEATURE_DATA_D3D11_OPTIONS1
title: D3D11_FEATURE_DATA_D3D11_OPTIONS1 (d3d11.h)
description: Describes Direct3D 11.2 feature options in the current graphics driver.
helpviewer_keywords: ["D3D11_FEATURE_DATA_D3D11_OPTIONS1","D3D11_FEATURE_DATA_D3D11_OPTIONS1 structure [Direct3D 11]","d3d11/D3D11_FEATURE_DATA_D3D11_OPTIONS1","direct3d11.d3d11_feature_data_d3d11_options1"]
old-location: direct3d11\d3d11_feature_data_d3d11_options1.htm
tech.root: direct3d11
ms.assetid: 940381BB-E8E6-416D-8F36-CC3591E70702
ms.date: 12/05/2018
ms.keywords: D3D11_FEATURE_DATA_D3D11_OPTIONS1, D3D11_FEATURE_DATA_D3D11_OPTIONS1 structure [Direct3D 11], d3d11/D3D11_FEATURE_DATA_D3D11_OPTIONS1, direct3d11.d3d11_feature_data_d3d11_options1
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
req.typenames: D3D11_FEATURE_DATA_D3D11_OPTIONS1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_FEATURE_DATA_D3D11_OPTIONS1
 - d3d11/D3D11_FEATURE_DATA_D3D11_OPTIONS1
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
 - D3D11_FEATURE_DATA_D3D11_OPTIONS1
---

## -description

> [!NOTE]
> This structure is supported by the Direct3D 11.2 runtime, which is available on Windows 8.1 and later operating systems.

Describes Direct3D 11.2 feature options in the current graphics driver.

## -struct-fields

### -field TiledResourcesTier

Type: <b><a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_tiled_resources_tier">D3D11_TILED_RESOURCES_TIER</a></b>

Specifies whether the hardware and driver support tiled resources. The runtime sets this member to a <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_tiled_resources_tier">D3D11_TILED_RESOURCES_TIER</a>-typed value that indicates if the hardware and driver support tiled resources and at what tier level.

### -field MinMaxFiltering

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Specifies whether the hardware and driver support the filtering options (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_filter">D3D11_FILTER</a>) of comparing the result to the minimum or maximum value during texture sampling. The runtime sets this member to <b>TRUE</b> if the hardware and driver support these filtering options.

### -field ClearViewAlsoSupportsDepthOnlyFormats

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Specifies whether the hardware and driver also support the <a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-clearview">ID3D11DeviceContext1::ClearView</a> method on depth formats. For info about valid depth formats, see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_depth_stencil_view_desc">D3D11_DEPTH_STENCIL_VIEW_DESC</a>.

### -field MapOnDefaultBuffers

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Specifies support for creating <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11buffer">ID3D11Buffer</a> resources that can be passed to the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-map">ID3D11DeviceContext::Map</a> and <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-unmap">ID3D11DeviceContext::Unmap</a> methods. This means that the <b>CPUAccessFlags</b> member of the <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_buffer_desc">D3D11_BUFFER_DESC</a> structure may be set with the desired <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_cpu_access_flag">D3D11_CPU_ACCESS_FLAG</a> elements when the <b>Usage</b> member of <b>D3D11_BUFFER_DESC</b> is set to <b>D3D11_USAGE_DEFAULT</b>. The runtime sets this member to <b>TRUE</b> if the hardware is capable of at least <b>D3D_FEATURE_LEVEL_11_0</b> and the graphics device driver supports mappable default buffers.

## -remarks

If the Direct3D API is the Direct3D 11.2 runtime and can support 11.2 features, <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport">ID3D11Device::CheckFeatureSupport</a> for <b>D3D11_FEATURE_D3D11_OPTIONS1</b> will return a SUCCESS code when valid parameters are passed. The members of <b>D3D11_FEATURE_DATA_D3D11_OPTIONS1</b> will be set appropriately based on the system's graphics hardware and graphics driver.

<h3><a id="Mappable_default_buffers"></a><a id="mappable_default_buffers"></a><a id="MAPPABLE_DEFAULT_BUFFERS"></a>Mappable default buffers</h3>
When creating a default buffer with <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_cpu_access_flag">D3D11_CPU_ACCESS_FLAG</a>, only the <b>D3D11_BIND_SHADER_RESOURCE</b> and <b>D3D11_BIND_UNORDERED_ACCESS</b> <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_bind_flag">bind flags</a> may be used.

The <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag">D3D11_RESOURCE_MISC_FLAG</a> cannot be used when creating resources with <b>D3D11_CPU_ACCESS</b> flags.

On non-unified memory architecture systems (discrete GPUs), apps should not use mappable default buffers if the compute shader code accesses the same byte in a default buffer more than once - sending the data across the bus multiple times eliminates the performance gained by mapping the default buffer instead of copying it.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-structures">Core Structures</a>

<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature">D3D11_FEATURE</a>