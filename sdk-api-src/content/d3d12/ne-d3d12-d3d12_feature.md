---
UID: NE:d3d12.D3D12_FEATURE
title: D3D12_FEATURE
author: windows-sdk-content
description: Specifies a Direct3D 12 feature or feature set to query about. When you want to query for the level to which an adapter supports a feature, pass one of these values to ID3D12Device::CheckFeatureSupport.
old-location: direct3d12\d3d12_feature.htm
tech.root: direct3d12
ms.assetid: 165ECFE0-1B18-4A26-8B9C-3CE53776A349
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: D3D12_FEATURE, D3D12_FEATURE enumeration, D3D12_FEATURE_ARCHITECTURE, D3D12_FEATURE_ARCHITECTURE1, D3D12_FEATURE_COMMAND_QUEUE_PRIORITY, D3D12_FEATURE_D3D12_OPTIONS, D3D12_FEATURE_D3D12_OPTIONS1, D3D12_FEATURE_D3D12_OPTIONS2, D3D12_FEATURE_D3D12_OPTIONS3, D3D12_FEATURE_D3D12_OPTIONS5, D3D12_FEATURE_EXISTING_HEAPS, D3D12_FEATURE_FEATURE_LEVELS, D3D12_FEATURE_FORMAT_INFO, D3D12_FEATURE_FORMAT_SUPPORT, D3D12_FEATURE_GPU_VIRTUAL_ADDRESS_SUPPORT, D3D12_FEATURE_MULTISAMPLE_QUALITY_LEVELS, D3D12_FEATURE_ROOT_SIGNATURE, D3D12_FEATURE_SHADER_CACHE, D3D12_FEATURE_SHADER_MODEL, d3d12/D3D12_FEATURE, d3d12/D3D12_FEATURE_ARCHITECTURE, d3d12/D3D12_FEATURE_ARCHITECTURE1, d3d12/D3D12_FEATURE_COMMAND_QUEUE_PRIORITY, d3d12/D3D12_FEATURE_D3D12_OPTIONS, d3d12/D3D12_FEATURE_D3D12_OPTIONS1, d3d12/D3D12_FEATURE_D3D12_OPTIONS2, d3d12/D3D12_FEATURE_D3D12_OPTIONS3, d3d12/D3D12_FEATURE_D3D12_OPTIONS5, d3d12/D3D12_FEATURE_EXISTING_HEAPS, d3d12/D3D12_FEATURE_FEATURE_LEVELS, d3d12/D3D12_FEATURE_FORMAT_INFO, d3d12/D3D12_FEATURE_FORMAT_SUPPORT, d3d12/D3D12_FEATURE_GPU_VIRTUAL_ADDRESS_SUPPORT, d3d12/D3D12_FEATURE_MULTISAMPLE_QUALITY_LEVELS, d3d12/D3D12_FEATURE_ROOT_SIGNATURE, d3d12/D3D12_FEATURE_SHADER_CACHE, d3d12/D3D12_FEATURE_SHADER_MODEL, direct3d12.d3d12_feature
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_FEATURE
product: Windows
targetos: Windows
req.typenames: D3D12_FEATURE
req.redist: 
---

# D3D12_FEATURE enumeration


## -description


Specifies a Direct3D 12 feature or feature set to query about. When you want to query for the level to which an adapter supports a feature, pass one of these values to <a href="https://msdn.microsoft.com/2E986E37-30C7-45FE-BC8B-A6DD5670938F">ID3D12Device::CheckFeatureSupport</a>.


## -enum-fields




### -field D3D12_FEATURE_D3D12_OPTIONS

Indicates a query for the level of support for basic Direct3D 12 feature options. The corresponding data structure for this value is <a href="https://msdn.microsoft.com/3193E3CC-C6CA-43D4-8D8C-41B7FCEE2BDF">D3D12_FEATURE_DATA_D3D12_OPTIONS</a>.


### -field D3D12_FEATURE_ARCHITECTURE

Indicates a query for the adapter's architectural details, so that your application can better optimize for certain adapter properties. The corresponding data structure for this value is <a href="https://msdn.microsoft.com/FA16A260-3CC9-4F32-A97B-8A561A01C138">D3D12_FEATURE_DATA_ARCHITECTURE</a>.

<div class="alert"><b>Note</b>  This value has been superseded by the <b>D3D_FEATURE_DATA_ARCHITECTURE1</b> value. If your application targets Windows 10, version 1703 (Creators' Update) or higher, then use the <b>D3D_FEATURE_DATA_ARCHITECTURE1</b> value instead.</div>
<div> </div>

### -field D3D12_FEATURE_FEATURE_LEVELS

Indicates a query for info about the <a href="https://msdn.microsoft.com/5ad0525c-249f-452d-950b-df8fa2addde2">feature levels</a> supported. The corresponding data structure for this value is <a href="https://msdn.microsoft.com/8C709889-0C7E-4D6D-84BD-1449BB8EA96A">D3D12_FEATURE_DATA_FEATURE_LEVELS</a>.


### -field D3D12_FEATURE_FORMAT_SUPPORT

Indicates a query for the resources supported by the current graphics driver for a given format. The corresponding data structure for this value is <a href="https://msdn.microsoft.com/6E4EB08F-0B60-4B1E-AD27-8F0AE2BD0766">D3D12_FEATURE_DATA_FORMAT_SUPPORT</a>.


### -field D3D12_FEATURE_MULTISAMPLE_QUALITY_LEVELS

Indicates a query for the image quality levels for a given format and sample count. The corresponding data structure for this value is <a href="https://msdn.microsoft.com/F3ECEF7C-F4A4-4134-9671-21AE488D8183">D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS</a>.


### -field D3D12_FEATURE_FORMAT_INFO

Indicates a query for the DXGI data format. The corresponding data structure for this value is <a href="https://msdn.microsoft.com/8695994A-CC83-451C-AD1B-65359656F3CC">D3D12_FEATURE_DATA_FORMAT_INFO</a>.


### -field D3D12_FEATURE_GPU_VIRTUAL_ADDRESS_SUPPORT

Indicates a query for the GPU's virtual address space limitations. The corresponding data structure for this value is <a href="https://msdn.microsoft.com/2CBED491-A8B6-47AE-8371-2081BAF85B83">D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT</a>.


### -field D3D12_FEATURE_SHADER_MODEL

Indicates a query for the supported shader model. The corresponding data structure for this value is <a href="https://msdn.microsoft.com/17978B9A-D21B-4A8A-B367-12F4ABC43A94">D3D12_FEATURE_DATA_SHADER_MODEL</a>.


### -field D3D12_FEATURE_D3D12_OPTIONS1

Indicates a query for the level of support for HLSL 6.0 wave operations. The corresponding data structure for this value is <a href="https://msdn.microsoft.com/39BF7632-AC73-471B-94F9-3128BD0DAB89">D3D12_FEATURE_DATA_D3D12_OPTIONS1</a>.


### -field D3D12_FEATURE_PROTECTED_RESOURCE_SESSION_SUPPORT


### -field D3D12_FEATURE_ROOT_SIGNATURE

Indicates a query for root signature version support. The corresponding data structure for this value is <a href="https://msdn.microsoft.com/3CC49B10-18B9-4A10-9013-D8F265FD1A28">D3D12_FEATURE_DATA_ROOT_SIGNATURE</a>.


### -field D3D12_FEATURE_ARCHITECTURE1

Indicates a query for each adapter's architectural details, so that your application can better optimize for certain adapter properties. The corresponding data structure for this value is <a href="https://msdn.microsoft.com/635091FE-2756-4648-958E-0C13BDD50851">D3D12_FEATURE_DATA_ARCHITECTURE1</a>.

<div class="alert"><b>Note</b>  This value supersedes the <b>D3D_FEATURE_DATA_ARCHITECTURE</b> value. If your application targets Windows 10, version 1703 (Creators' Update) or higher, then use <b>D3D_FEATURE_DATA_ARCHITECTURE1</b>.</div>
<div> </div>

### -field D3D12_FEATURE_D3D12_OPTIONS2

Indicates a query for the level of support for depth-bounds tests and programmable sample positions. The corresponding data structure for this value is <a href="https://msdn.microsoft.com/E45DA471-E0A9-47BF-8AE5-4B8BA4B38337">D3D12_FEATURE_DATA_D3D12_OPTIONS2</a>.


### -field D3D12_FEATURE_SHADER_CACHE

Indicates a query for the level of support for shader caching. The corresponding data structure for this value is <a href="https://msdn.microsoft.com/B6BC2E8F-04FE-4855-87C2-89A054519AFD">D3D12_FEATURE_DATA_SHADER_CACHE</a>.


### -field D3D12_FEATURE_COMMAND_QUEUE_PRIORITY

Indicates a query for the adapter's support for prioritization of different command queue types. The corresponding data structure for this value is <a href="https://msdn.microsoft.com/70DB58DB-7EE0-4E5C-8B24-22DA9347A80F">D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY</a>.


### -field D3D12_FEATURE_D3D12_OPTIONS3

Indicates a query for the level of support for timestamp queries, format-casting, immediate write, view instancing, and barycentrics. The corresponding data structure for this value is <a href="https://msdn.microsoft.com/4BA37E6A-124D-4808-8005-CC049B8EE165">D3D12_FEATURE_DATA_D3D12_OPTIONS3</a>.


### -field D3D12_FEATURE_EXISTING_HEAPS

Indicates a query for whether or not the adapter supports creating heaps from existing system memory. The corresponding data structure for this value is <a href="https://msdn.microsoft.com/7F0D0FAD-BF29-43AD-95FA-85B9719C4782">D3D12_FEATURE_DATA_EXISTING_HEAPS</a>.
          


### -field D3D12_FEATURE_D3D12_OPTIONS4


### -field D3D12_FEATURE_SERIALIZATION


### -field D3D12_FEATURE_CROSS_NODE


### -field D3D12_FEATURE_D3D12_OPTIONS5

Starting with Windows 10, version 1809 (10.0; Build 17763), indicates a query for the level of support for render passes, ray tracing, and shader-resource view tier 3 tiled resources. The corresponding data structure for this value is <a href="https://msdn.microsoft.com/7B786C22-56C1-44A0-BE67-DE04EB367FD2">D3D12_FEATURE_DATA_D3D12_OPTIONS5</a>.


## -remarks



Use a constant from  this enumeration in a call to <a href="https://msdn.microsoft.com/2E986E37-30C7-45FE-BC8B-A6DD5670938F">ID3D12Device::CheckFeatureSupport</a> to query a driver about support for various Direct3D 12 features.
        Each value in this enumeration has a corresponding data structure that you must pass (by pointer reference) in the <i>pFeatureSupportData</i> parameter
        of <b>ID3D12Device::CheckFeatureSupport</b>.




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>



<a href="https://msdn.microsoft.com/2E986E37-30C7-45FE-BC8B-A6DD5670938F">ID3D12Device::CheckFeatureSupport</a>
 

 

