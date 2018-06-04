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

# D3D11_SHADER_TRACKING_OPTION enumeration


## -description


Options that specify how to perform shader debug tracking.


## -enum-fields




### -field D3D11_SHADER_TRACKING_OPTION_IGNORE

No debug tracking is performed.


### -field D3D11_SHADER_TRACKING_OPTION_TRACK_UNINITIALIZED

Track the reading of uninitialized data.


### -field D3D11_SHADER_TRACKING_OPTION_TRACK_RAW

Track read-after-write hazards.


### -field D3D11_SHADER_TRACKING_OPTION_TRACK_WAR

Track write-after-read hazards.


### -field D3D11_SHADER_TRACKING_OPTION_TRACK_WAW

Track write-after-write hazards.


### -field D3D11_SHADER_TRACKING_OPTION_ALLOW_SAME

Track that hazards are allowed in which data is written but the value does not change.


### -field D3D11_SHADER_TRACKING_OPTION_TRACK_ATOMIC_CONSISTENCY

Track that only one type of atomic operation is used on an address.


### -field D3D11_SHADER_TRACKING_OPTION_TRACK_RAW_ACROSS_THREADGROUPS

Track read-after-write hazards across thread groups.


### -field D3D11_SHADER_TRACKING_OPTION_TRACK_WAR_ACROSS_THREADGROUPS

Track write-after-read hazards across thread groups.


### -field D3D11_SHADER_TRACKING_OPTION_TRACK_WAW_ACROSS_THREADGROUPS

Track write-after-write hazards across thread groups.


### -field D3D11_SHADER_TRACKING_OPTION_TRACK_ATOMIC_CONSISTENCY_ACROSS_THREADGROUPS

Track that only one type of atomic operation is used on an address across thread groups.


### -field D3D11_SHADER_TRACKING_OPTION_UAV_SPECIFIC_FLAGS

Track hazards that are specific to unordered access views (UAVs).


### -field D3D11_SHADER_TRACKING_OPTION_ALL_HAZARDS

Track all hazards.


### -field D3D11_SHADER_TRACKING_OPTION_ALL_HAZARDS_ALLOWING_SAME

Track all hazards and track that hazards are allowed in which data is written but the value does not change.


### -field D3D11_SHADER_TRACKING_OPTION_ALL_OPTIONS


            All of the preceding tracking options are set except <b>D3D11_SHADER_TRACKING_OPTION_IGNORE</b>.
          


## -remarks




          This enumeration is used by the following methods:
        

<ul>
<li>
<a href="https://msdn.microsoft.com/A54AAC4C-CD38-4326-AF99-9FB74CC0A1A0">ID3D11RefDefaultTrackingOptions::SetTrackingOptions</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2C782DBE-BA76-4D2E-82D6-1A03941B2FB1">ID3D11RefTrackingOptions::SetTrackingOptions</a>
</li>
<li>
<a href="https://msdn.microsoft.com/F62FCA38-AE44-427B-95B4-252AE800845C">ID3D11TracingDevice::SetShaderTrackingOptions</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ABB83CE4-D612-4797-A9AD-F3C2954E669D">ID3D11TracingDevice::SetShaderTrackingOptionsByType</a>
</li>
</ul>
<div class="alert"><b>Note</b>  
        This API requires the Windows Software Development Kit (SDK) for Windows 8.
      </div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/0fd0456b-2638-4b4c-8a34-a3e104a1a034">Layer Enumerations</a>
 

 

