---
UID: NE:d3d11sdklayers.D3D11_SHADER_TRACKING_RESOURCE_TYPE
title: D3D11_SHADER_TRACKING_RESOURCE_TYPE (d3d11sdklayers.h)
description: Indicates which resource types to track.
helpviewer_keywords: ["D3D11_SHADER_TRACKING_RESOURCE_TYPE","D3D11_SHADER_TRACKING_RESOURCE_TYPE enumeration [Direct3D 11]","D3D11_SHADER_TRACKING_RESOURCE_TYPE_ALL","D3D11_SHADER_TRACKING_RESOURCE_TYPE_ALL_DEVICEMEMORY","D3D11_SHADER_TRACKING_RESOURCE_TYPE_ALL_SHARED_MEMORY","D3D11_SHADER_TRACKING_RESOURCE_TYPE_GROUPSHARED_MEMORY","D3D11_SHADER_TRACKING_RESOURCE_TYPE_GROUPSHARED_NON_UAV","D3D11_SHADER_TRACKING_RESOURCE_TYPE_NONE","D3D11_SHADER_TRACKING_RESOURCE_TYPE_NON_UAV_DEVICEMEMORY","D3D11_SHADER_TRACKING_RESOURCE_TYPE_UAV_DEVICEMEMORY","d3d11sdklayers/D3D11_SHADER_TRACKING_RESOURCE_TYPE","d3d11sdklayers/D3D11_SHADER_TRACKING_RESOURCE_TYPE_ALL","d3d11sdklayers/D3D11_SHADER_TRACKING_RESOURCE_TYPE_ALL_DEVICEMEMORY","d3d11sdklayers/D3D11_SHADER_TRACKING_RESOURCE_TYPE_ALL_SHARED_MEMORY","d3d11sdklayers/D3D11_SHADER_TRACKING_RESOURCE_TYPE_GROUPSHARED_MEMORY","d3d11sdklayers/D3D11_SHADER_TRACKING_RESOURCE_TYPE_GROUPSHARED_NON_UAV","d3d11sdklayers/D3D11_SHADER_TRACKING_RESOURCE_TYPE_NONE","d3d11sdklayers/D3D11_SHADER_TRACKING_RESOURCE_TYPE_NON_UAV_DEVICEMEMORY","d3d11sdklayers/D3D11_SHADER_TRACKING_RESOURCE_TYPE_UAV_DEVICEMEMORY","direct3d11.d3d11_shader_tracking_resource_type"]
old-location: direct3d11\d3d11_shader_tracking_resource_type.htm
tech.root: direct3d11
ms.assetid: 148303AC-E373-4D41-BDF5-0E17B2A3D366
ms.date: 12/05/2018
ms.keywords: D3D11_SHADER_TRACKING_RESOURCE_TYPE, D3D11_SHADER_TRACKING_RESOURCE_TYPE enumeration [Direct3D 11], D3D11_SHADER_TRACKING_RESOURCE_TYPE_ALL, D3D11_SHADER_TRACKING_RESOURCE_TYPE_ALL_DEVICEMEMORY, D3D11_SHADER_TRACKING_RESOURCE_TYPE_ALL_SHARED_MEMORY, D3D11_SHADER_TRACKING_RESOURCE_TYPE_GROUPSHARED_MEMORY, D3D11_SHADER_TRACKING_RESOURCE_TYPE_GROUPSHARED_NON_UAV, D3D11_SHADER_TRACKING_RESOURCE_TYPE_NONE, D3D11_SHADER_TRACKING_RESOURCE_TYPE_NON_UAV_DEVICEMEMORY, D3D11_SHADER_TRACKING_RESOURCE_TYPE_UAV_DEVICEMEMORY, d3d11sdklayers/D3D11_SHADER_TRACKING_RESOURCE_TYPE, d3d11sdklayers/D3D11_SHADER_TRACKING_RESOURCE_TYPE_ALL, d3d11sdklayers/D3D11_SHADER_TRACKING_RESOURCE_TYPE_ALL_DEVICEMEMORY, d3d11sdklayers/D3D11_SHADER_TRACKING_RESOURCE_TYPE_ALL_SHARED_MEMORY, d3d11sdklayers/D3D11_SHADER_TRACKING_RESOURCE_TYPE_GROUPSHARED_MEMORY, d3d11sdklayers/D3D11_SHADER_TRACKING_RESOURCE_TYPE_GROUPSHARED_NON_UAV, d3d11sdklayers/D3D11_SHADER_TRACKING_RESOURCE_TYPE_NONE, d3d11sdklayers/D3D11_SHADER_TRACKING_RESOURCE_TYPE_NON_UAV_DEVICEMEMORY, d3d11sdklayers/D3D11_SHADER_TRACKING_RESOURCE_TYPE_UAV_DEVICEMEMORY, direct3d11.d3d11_shader_tracking_resource_type
req.header: d3d11sdklayers.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: D3D11_SHADER_TRACKING_RESOURCE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_SHADER_TRACKING_RESOURCE_TYPE
 - d3d11sdklayers/D3D11_SHADER_TRACKING_RESOURCE_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11SDKLayers.h
api_name:
 - D3D11_SHADER_TRACKING_RESOURCE_TYPE
---

# D3D11_SHADER_TRACKING_RESOURCE_TYPE enumeration


## -description

Indicates which resource types to track.

## -enum-fields

### -field D3D11_SHADER_TRACKING_RESOURCE_TYPE_NONE:0

No resource types are tracked.

### -field D3D11_SHADER_TRACKING_RESOURCE_TYPE_UAV_DEVICEMEMORY:1

Track device memory that is created with unordered access view (UAV) bind flags.

### -field D3D11_SHADER_TRACKING_RESOURCE_TYPE_NON_UAV_DEVICEMEMORY:2

Track device memory that is created without UAV bind flags.

### -field D3D11_SHADER_TRACKING_RESOURCE_TYPE_ALL_DEVICEMEMORY:3

Track all device memory.

### -field D3D11_SHADER_TRACKING_RESOURCE_TYPE_GROUPSHARED_MEMORY:4

Track all shaders that use group shared memory.

### -field D3D11_SHADER_TRACKING_RESOURCE_TYPE_ALL_SHARED_MEMORY:5

Track all device memory except device memory that is created without UAV bind flags.

### -field D3D11_SHADER_TRACKING_RESOURCE_TYPE_GROUPSHARED_NON_UAV:6

Track all device memory except device memory that is created with UAV bind flags.

### -field D3D11_SHADER_TRACKING_RESOURCE_TYPE_ALL:7

Track all memory on the device.

## -remarks

The <a href="/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11tracingdevice-setshadertrackingoptionsbytype">ID3D11TracingDevice::SetShaderTrackingOptionsByType</a> or <a href="/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11refdefaulttrackingoptions-settrackingoptions">ID3D11RefDefaultTrackingOptions::SetTrackingOptions</a> method tracks a specific type of resource.

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-layer-enums">Layer Enumerations</a>
