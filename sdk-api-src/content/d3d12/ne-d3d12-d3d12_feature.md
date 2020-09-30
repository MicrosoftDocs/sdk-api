---
UID: NE:d3d12.D3D12_FEATURE
title: D3D12_FEATURE
description: Defines constants that specify a Direct3D 12 feature or feature set to query about.
helpviewer_keywords: ["D3D12_FEATURE","D3D12_FEATURE enumeration","D3D12_FEATURE_ARCHITECTURE","D3D12_FEATURE_FEATURE_LEVELS","D3D12_FEATURE_FORMAT_SUPPORT","D3D12_FEATURE_MULTISAMPLE_QUALITY_LEVELS","D3D12_FEATURE_FORMAT_INFO","D3D12_FEATURE_GPU_VIRTUAL_ADDRESS_SUPPORT","D3D12_FEATURE_SHADER_MODEL","D3D12_FEATURE_D3D12_OPTIONS1","D3D12_FEATURE_PROTECTED_RESOURCE_SESSION_SUPPORT","D3D12_FEATURE_ROOT_SIGNATURE","D3D12_FEATURE_ARCHITECTURE1","D3D12_FEATURE_D3D12_OPTIONS2","D3D12_FEATURE_SHADER_CACHE","D3D12_FEATURE_COMMAND_QUEUE_PRIORITY","D3D12_FEATURE_D3D12_OPTIONS3","D3D12_FEATURE_EXISTING_HEAPS","D3D12_FEATURE_D3D12_OPTIONS4","D3D12_FEATURE_SERIALIZATION","D3D12_FEATURE_CROSS_NODE","D3D12_FEATURE_D3D12_OPTIONS5","D3D12_FEATURE_D3D12_OPTIONS6","D3D12_FEATURE_QUERY_META_COMMAND","d3d12/D3D12_FEATURE_ARCHITECTURE","d3d12/D3D12_FEATURE_FEATURE_LEVELS","d3d12/D3D12_FEATURE_FORMAT_SUPPORT","d3d12/D3D12_FEATURE_MULTISAMPLE_QUALITY_LEVELS","d3d12/D3D12_FEATURE_FORMAT_INFO","d3d12/D3D12_FEATURE_GPU_VIRTUAL_ADDRESS_SUPPORT","d3d12/D3D12_FEATURE_SHADER_MODEL","d3d12/D3D12_FEATURE_D3D12_OPTIONS1","d3d12/D3D12_FEATURE_PROTECTED_RESOURCE_SESSION_SUPPORT","d3d12/D3D12_FEATURE_ROOT_SIGNATURE","d3d12/D3D12_FEATURE_ARCHITECTURE1","d3d12/D3D12_FEATURE_D3D12_OPTIONS2","d3d12/D3D12_FEATURE_SHADER_CACHE","d3d12/D3D12_FEATURE_COMMAND_QUEUE_PRIORITY","d3d12/D3D12_FEATURE_D3D12_OPTIONS3","d3d12/D3D12_FEATURE_EXISTING_HEAPS","d3d12/D3D12_FEATURE_D3D12_OPTIONS4","d3d12/D3D12_FEATURE_SERIALIZATION","d3d12/D3D12_FEATURE_CROSS_NODE","d3d12/D3D12_FEATURE_D3D12_OPTIONS5","d3d12/D3D12_FEATURE_D3D12_OPTIONS6","d3d12/D3D12_FEATURE_QUERY_META_COMMAND","direct3d12.d3d12_feature"]
old-location: direct3d12\d3d12_feature.htm
tech.root: direct3d12
ms.assetid: 165ECFE0-1B18-4A26-8B9C-3CE53776A349
ms.date: 09/19/2019
ms.keywords: D3D12_FEATURE, D3D12_FEATURE enumeration, D3D12_FEATURE_ARCHITECTURE, D3D12_FEATURE_FEATURE_LEVELS, D3D12_FEATURE_FORMAT_SUPPORT, D3D12_FEATURE_MULTISAMPLE_QUALITY_LEVELS, D3D12_FEATURE_FORMAT_INFO, D3D12_FEATURE_GPU_VIRTUAL_ADDRESS_SUPPORT, D3D12_FEATURE_SHADER_MODEL, D3D12_FEATURE_D3D12_OPTIONS1, D3D12_FEATURE_PROTECTED_RESOURCE_SESSION_SUPPORT, D3D12_FEATURE_ROOT_SIGNATURE, D3D12_FEATURE_ARCHITECTURE1, D3D12_FEATURE_D3D12_OPTIONS2, D3D12_FEATURE_SHADER_CACHE, D3D12_FEATURE_COMMAND_QUEUE_PRIORITY, D3D12_FEATURE_D3D12_OPTIONS3, D3D12_FEATURE_EXISTING_HEAPS, D3D12_FEATURE_D3D12_OPTIONS4, D3D12_FEATURE_SERIALIZATION, D3D12_FEATURE_CROSS_NODE, D3D12_FEATURE_D3D12_OPTIONS5, D3D12_FEATURE_D3D12_OPTIONS6, D3D12_FEATURE_QUERY_META_COMMAND, d3d12/D3D12_FEATURE_ARCHITECTURE, d3d12/D3D12_FEATURE_FEATURE_LEVELS, d3d12/D3D12_FEATURE_FORMAT_SUPPORT, d3d12/D3D12_FEATURE_MULTISAMPLE_QUALITY_LEVELS, d3d12/D3D12_FEATURE_FORMAT_INFO, d3d12/D3D12_FEATURE_GPU_VIRTUAL_ADDRESS_SUPPORT, d3d12/D3D12_FEATURE_SHADER_MODEL, d3d12/D3D12_FEATURE_D3D12_OPTIONS1, d3d12/D3D12_FEATURE_PROTECTED_RESOURCE_SESSION_SUPPORT, d3d12/D3D12_FEATURE_ROOT_SIGNATURE, d3d12/D3D12_FEATURE_ARCHITECTURE1, d3d12/D3D12_FEATURE_D3D12_OPTIONS2, d3d12/D3D12_FEATURE_SHADER_CACHE, d3d12/D3D12_FEATURE_COMMAND_QUEUE_PRIORITY, d3d12/D3D12_FEATURE_D3D12_OPTIONS3, d3d12/D3D12_FEATURE_EXISTING_HEAPS, d3d12/D3D12_FEATURE_D3D12_OPTIONS4, d3d12/D3D12_FEATURE_SERIALIZATION, d3d12/D3D12_FEATURE_CROSS_NODE, d3d12/D3D12_FEATURE_D3D12_OPTIONS5, d3d12/D3D12_FEATURE_D3D12_OPTIONS6, d3d12/D3D12_FEATURE_QUERY_META_COMMAND, direct3d12.d3d12_feature
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
req.typenames: D3D12_FEATURE
req.redist: 
f1_keywords:
 - D3D12_FEATURE
 - d3d12/D3D12_FEATURE
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
 - D3D12_FEATURE
---

## -description

Defines constants that specify a Direct3D 12 feature or feature set to query about. When you want to query for the level to which an adapter supports a feature, pass one of these values to [ID3D12Device::CheckFeatureSupport](./nf-d3d12-id3d12device-checkfeaturesupport.md).

## -enum-fields

### -field D3D12_FEATURE_D3D12_OPTIONS

Indicates a query for the level of support for basic Direct3D 12 feature options. The corresponding data structure for this value is <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options">D3D12_FEATURE_DATA_D3D12_OPTIONS</a>.

### -field D3D12_FEATURE_ARCHITECTURE

Indicates a query for the adapter's architectural details, so that your application can better optimize for certain adapter properties. The corresponding data structure for this value is <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_architecture">D3D12_FEATURE_DATA_ARCHITECTURE</a>.

<div class="alert"><b>Note</b>  This value has been superseded by the <b>D3D_FEATURE_DATA_ARCHITECTURE1</b> value. If your application targets Windows 10, version 1703 (Creators' Update) or higher, then use the <b>D3D_FEATURE_DATA_ARCHITECTURE1</b> value instead.</div>
<div> </div>

### -field D3D12_FEATURE_FEATURE_LEVELS

Indicates a query for info about the <a href="/windows/win32/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature levels</a> supported. The corresponding data structure for this value is <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_feature_levels">D3D12_FEATURE_DATA_FEATURE_LEVELS</a>.

### -field D3D12_FEATURE_FORMAT_SUPPORT

Indicates a query for the resources supported by the current graphics driver for a given format. The corresponding data structure for this value is <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_format_support">D3D12_FEATURE_DATA_FORMAT_SUPPORT</a>.

### -field D3D12_FEATURE_MULTISAMPLE_QUALITY_LEVELS

Indicates a query for the image quality levels for a given format and sample count. The corresponding data structure for this value is <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_multisample_quality_levels">D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS</a>.

### -field D3D12_FEATURE_FORMAT_INFO

Indicates a query for the DXGI data format. The corresponding data structure for this value is <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_format_info">D3D12_FEATURE_DATA_FORMAT_INFO</a>.

### -field D3D12_FEATURE_GPU_VIRTUAL_ADDRESS_SUPPORT

Indicates a query for the GPU's virtual address space limitations. The corresponding data structure for this value is <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support">D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT</a>.

### -field D3D12_FEATURE_SHADER_MODEL

Indicates a query for the supported shader model. The corresponding data structure for this value is <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_shader_model">D3D12_FEATURE_DATA_SHADER_MODEL</a>.

### -field D3D12_FEATURE_D3D12_OPTIONS1

Indicates a query for the level of support for HLSL 6.0 wave operations. The corresponding data structure for this value is <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1">D3D12_FEATURE_DATA_D3D12_OPTIONS1</a>.

### -field D3D12_FEATURE_PROTECTED_RESOURCE_SESSION_SUPPORT

Indicates a query for the level of support for protected resource sessions. The corresponding data structure for this value is <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_protected_resource_session_support">D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_SUPPORT</a>.

### -field D3D12_FEATURE_ROOT_SIGNATURE

Indicates a query for root signature version support. The corresponding data structure for this value is <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_root_signature">D3D12_FEATURE_DATA_ROOT_SIGNATURE</a>.

### -field D3D12_FEATURE_ARCHITECTURE1

Indicates a query for each adapter's architectural details, so that your application can better optimize for certain adapter properties. The corresponding data structure for this value is <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_architecture1">D3D12_FEATURE_DATA_ARCHITECTURE1</a>.

<div class="alert"><b>Note</b>  This value supersedes the <b>D3D_FEATURE_DATA_ARCHITECTURE</b> value. If your application targets Windows 10, version 1703 (Creators' Update) or higher, then use <b>D3D_FEATURE_DATA_ARCHITECTURE1</b>.</div>
<div> </div>

### -field D3D12_FEATURE_D3D12_OPTIONS2

Indicates a query for the level of support for depth-bounds tests and programmable sample positions. The corresponding data structure for this value is <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options2">D3D12_FEATURE_DATA_D3D12_OPTIONS2</a>.

### -field D3D12_FEATURE_SHADER_CACHE

Indicates a query for the level of support for shader caching. The corresponding data structure for this value is <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_shader_cache">D3D12_FEATURE_DATA_SHADER_CACHE</a>.

### -field D3D12_FEATURE_COMMAND_QUEUE_PRIORITY

Indicates a query for the adapter's support for prioritization of different command queue types. The corresponding data structure for this value is <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_command_queue_priority">D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY</a>.

### -field D3D12_FEATURE_D3D12_OPTIONS3

Indicates a query for the level of support for timestamp queries, format-casting, immediate write, view instancing, and barycentrics. The corresponding data structure for this value is <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3">D3D12_FEATURE_DATA_D3D12_OPTIONS3</a>.

### -field D3D12_FEATURE_EXISTING_HEAPS

Indicates a query for whether or not the adapter supports creating heaps from existing system memory. The corresponding data structure for this value is <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_existing_heaps">D3D12_FEATURE_DATA_EXISTING_HEAPS</a>.

### -field D3D12_FEATURE_D3D12_OPTIONS4

Indicates a query for the level of support for 64KB-aligned MSAA textures, cross-API sharing, and native 16-bit shader operations. The corresponding data structure for this value is <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options4">D3D12_FEATURE_DATA_D3D12_OPTIONS4</a>.

### -field D3D12_FEATURE_SERIALIZATION

Indicates a query for the level of support for heap serialization. The corresponding data structure for this value is <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_serialization">D3D12_FEATURE_DATA_SERIALIZATION</a>.

### -field D3D12_FEATURE_CROSS_NODE

Indicates a query for the level of support for the sharing of resources between different adapters&mdash;for example, multiple GPUs. The corresponding data structure for this value is <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_cross_node">D3D12_FEATURE_DATA_CROSS_NODE</a>.

### -field D3D12_FEATURE_D3D12_OPTIONS5

Starting with Windows 10, version 1809 (10.0; Build 17763), indicates a query for the level of support for render passes, ray tracing, and shader-resource view tier 3 tiled resources. The corresponding data structure for this value is <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options5">D3D12_FEATURE_DATA_D3D12_OPTIONS5</a>.

### -field D3D12_FEATURE_D3D12_OPTIONS6

Starting with Windows 10, version 1903 (10.0; Build 18362), indicates a query for the level of support for variable-rate shading (VRS), and indicates whether or not background processing is supported. For more info, see <a href="/windows/win32/direct3d12/vrs">Variable-rate shading (VRS)</a>, and the <a href="https://microsoft.github.io/DirectX-Specs/d3d/BackgroundProcessing.html">Direct3D 12 background processing spec</a>.

### -field D3D12_FEATURE_QUERY_META_COMMAND

Indicates a query for the level of support for metacommands. The corresponding data structure for this value is <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_query_meta_command">D3D12_FEATURE_DATA_QUERY_META_COMMAND</a>.

## -remarks

Use a constant from  this enumeration in a call to [ID3D12Device::CheckFeatureSupport](./nf-d3d12-id3d12device-checkfeaturesupport.md) to query a driver about support for various Direct3D 12 features. Each value in this enumeration has a corresponding data structure that you must pass (by pointer reference) in the *pFeatureSupportData* parameter of **ID3D12Device::CheckFeatureSupport**.

## -see-also

[Core enumerations](/windows/win32/direct3d12/direct3d-12-enumerations)

[ID3D12Device::CheckFeatureSupport](./nf-d3d12-id3d12device-checkfeaturesupport.md)