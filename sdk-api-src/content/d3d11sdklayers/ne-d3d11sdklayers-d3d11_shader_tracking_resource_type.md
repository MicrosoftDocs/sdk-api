---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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



The <a href="https://msdn.microsoft.com/ABB83CE4-D612-4797-A9AD-F3C2954E669D">ID3D11TracingDevice::SetShaderTrackingOptionsByType</a> or <a href="https://msdn.microsoft.com/A54AAC4C-CD38-4326-AF99-9FB74CC0A1A0">ID3D11RefDefaultTrackingOptions::SetTrackingOptions</a> method tracks a specific type of resource.

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/0fd0456b-2638-4b4c-8a34-a3e104a1a034">Layer Enumerations</a>
 

 

