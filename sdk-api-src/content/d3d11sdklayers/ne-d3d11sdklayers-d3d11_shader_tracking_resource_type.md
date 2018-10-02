---
UID: NE:d3d11sdklayers.D3D11_SHADER_TRACKING_RESOURCE_TYPE
title: D3D11_SHADER_TRACKING_RESOURCE_TYPE
author: windows-sdk-content
description: Indicates which resource types to track.
old-location: direct3d11\d3d11_shader_tracking_resource_type.htm
tech.root: direct3d11
ms.assetid: 148303AC-E373-4D41-BDF5-0E17B2A3D366
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: D3D11_SHADER_TRACKING_RESOURCE_TYPE, D3D11_SHADER_TRACKING_RESOURCE_TYPE enumeration [Direct3D 11], D3D11_SHADER_TRACKING_RESOURCE_TYPE_ALL, D3D11_SHADER_TRACKING_RESOURCE_TYPE_ALL_DEVICEMEMORY, D3D11_SHADER_TRACKING_RESOURCE_TYPE_ALL_SHARED_MEMORY, D3D11_SHADER_TRACKING_RESOURCE_TYPE_GROUPSHARED_MEMORY, D3D11_SHADER_TRACKING_RESOURCE_TYPE_GROUPSHARED_NON_UAV, D3D11_SHADER_TRACKING_RESOURCE_TYPE_NONE, D3D11_SHADER_TRACKING_RESOURCE_TYPE_NON_UAV_DEVICEMEMORY, D3D11_SHADER_TRACKING_RESOURCE_TYPE_UAV_DEVICEMEMORY, d3d11sdklayers/D3D11_SHADER_TRACKING_RESOURCE_TYPE, d3d11sdklayers/D3D11_SHADER_TRACKING_RESOURCE_TYPE_ALL, d3d11sdklayers/D3D11_SHADER_TRACKING_RESOURCE_TYPE_ALL_DEVICEMEMORY, d3d11sdklayers/D3D11_SHADER_TRACKING_RESOURCE_TYPE_ALL_SHARED_MEMORY, d3d11sdklayers/D3D11_SHADER_TRACKING_RESOURCE_TYPE_GROUPSHARED_MEMORY, d3d11sdklayers/D3D11_SHADER_TRACKING_RESOURCE_TYPE_GROUPSHARED_NON_UAV, d3d11sdklayers/D3D11_SHADER_TRACKING_RESOURCE_TYPE_NONE, d3d11sdklayers/D3D11_SHADER_TRACKING_RESOURCE_TYPE_NON_UAV_DEVICEMEMORY, d3d11sdklayers/D3D11_SHADER_TRACKING_RESOURCE_TYPE_UAV_DEVICEMEMORY, direct3d11.d3d11_shader_tracking_resource_type
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11SDKLayers.h
api_name:
 - D3D11_SHADER_TRACKING_RESOURCE_TYPE
product: Windows
targetos: Windows
req.typenames: D3D11_SHADER_TRACKING_RESOURCE_TYPE
req.redist: 
---

# D3D11_SHADER_TRACKING_RESOURCE_TYPE enumeration


## -description


Indicates which resource types to track.


## -enum-fields




### -field D3D11_SHADER_TRACKING_RESOURCE_TYPE_NONE

No resource types are tracked.


### -field D3D11_SHADER_TRACKING_RESOURCE_TYPE_UAV_DEVICEMEMORY

Track device memory that is created with unordered access view (UAV) bind flags.


### -field D3D11_SHADER_TRACKING_RESOURCE_TYPE_NON_UAV_DEVICEMEMORY

Track device memory that is created without UAV bind flags.


### -field D3D11_SHADER_TRACKING_RESOURCE_TYPE_ALL_DEVICEMEMORY

Track all device memory.


### -field D3D11_SHADER_TRACKING_RESOURCE_TYPE_GROUPSHARED_MEMORY

Track all shaders that use group shared memory.


### -field D3D11_SHADER_TRACKING_RESOURCE_TYPE_ALL_SHARED_MEMORY

Track all device memory except device memory that is created without UAV bind flags.


### -field D3D11_SHADER_TRACKING_RESOURCE_TYPE_GROUPSHARED_NON_UAV

Track all device memory except device memory that is created with UAV bind flags.


### -field D3D11_SHADER_TRACKING_RESOURCE_TYPE_ALL

Track all memory on the device.


## -remarks



The <a href="https://msdn.microsoft.com/en-us/library/Hh446874(v=VS.85).aspx">ID3D11TracingDevice::SetShaderTrackingOptionsByType</a> or <a href="https://msdn.microsoft.com/en-us/library/Hh446834(v=VS.85).aspx">ID3D11RefDefaultTrackingOptions::SetTrackingOptions</a> method tracks a specific type of resource.

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476157(v=VS.85).aspx">Layer Enumerations</a>
 

 

