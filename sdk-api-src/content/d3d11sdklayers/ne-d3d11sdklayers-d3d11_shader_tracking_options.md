---
UID: NE:d3d11sdklayers.D3D11_SHADER_TRACKING_OPTION
title: D3D11_SHADER_TRACKING_OPTIONS (d3d11sdklayers.h)
author: windows-sdk-content
description: Options that specify how to perform shader debug tracking.
old-location: direct3d11\d3d11_shader_tracking_options.htm
tech.root: direct3d11
ms.assetid: 20C152CD-B155-4B46-8F41-EDDEC60494DF
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D11_SHADER_TRACKING_OPTIONS, D3D11_SHADER_TRACKING_OPTIONS enumeration [Direct3D 11], D3D11_SHADER_TRACKING_OPTION_ALLOW_SAME, D3D11_SHADER_TRACKING_OPTION_ALL_HAZARDS, D3D11_SHADER_TRACKING_OPTION_ALL_HAZARDS_ALLOWING_SAME, D3D11_SHADER_TRACKING_OPTION_ALL_OPTIONS, D3D11_SHADER_TRACKING_OPTION_IGNORE, D3D11_SHADER_TRACKING_OPTION_TRACK_ATOMIC_CONSISTENCY, D3D11_SHADER_TRACKING_OPTION_TRACK_ATOMIC_CONSISTENCY_ACROSS_THREADGROUPS, D3D11_SHADER_TRACKING_OPTION_TRACK_RAW, D3D11_SHADER_TRACKING_OPTION_TRACK_RAW_ACROSS_THREADGROUPS, D3D11_SHADER_TRACKING_OPTION_TRACK_UNINITIALIZED, D3D11_SHADER_TRACKING_OPTION_TRACK_WAR, D3D11_SHADER_TRACKING_OPTION_TRACK_WAR_ACROSS_THREADGROUPS, D3D11_SHADER_TRACKING_OPTION_TRACK_WAW, D3D11_SHADER_TRACKING_OPTION_TRACK_WAW_ACROSS_THREADGROUPS, D3D11_SHADER_TRACKING_OPTION_UAV_SPECIFIC_FLAGS, d3d11sdklayers/D3D11_SHADER_TRACKING_OPTIONS, d3d11sdklayers/D3D11_SHADER_TRACKING_OPTION_ALLOW_SAME, d3d11sdklayers/D3D11_SHADER_TRACKING_OPTION_ALL_HAZARDS, d3d11sdklayers/D3D11_SHADER_TRACKING_OPTION_ALL_HAZARDS_ALLOWING_SAME, d3d11sdklayers/D3D11_SHADER_TRACKING_OPTION_ALL_OPTIONS, d3d11sdklayers/D3D11_SHADER_TRACKING_OPTION_IGNORE, d3d11sdklayers/D3D11_SHADER_TRACKING_OPTION_TRACK_ATOMIC_CONSISTENCY, d3d11sdklayers/D3D11_SHADER_TRACKING_OPTION_TRACK_ATOMIC_CONSISTENCY_ACROSS_THREADGROUPS, d3d11sdklayers/D3D11_SHADER_TRACKING_OPTION_TRACK_RAW, d3d11sdklayers/D3D11_SHADER_TRACKING_OPTION_TRACK_RAW_ACROSS_THREADGROUPS, d3d11sdklayers/D3D11_SHADER_TRACKING_OPTION_TRACK_UNINITIALIZED, d3d11sdklayers/D3D11_SHADER_TRACKING_OPTION_TRACK_WAR, d3d11sdklayers/D3D11_SHADER_TRACKING_OPTION_TRACK_WAR_ACROSS_THREADGROUPS, d3d11sdklayers/D3D11_SHADER_TRACKING_OPTION_TRACK_WAW, d3d11sdklayers/D3D11_SHADER_TRACKING_OPTION_TRACK_WAW_ACROSS_THREADGROUPS, d3d11sdklayers/D3D11_SHADER_TRACKING_OPTION_UAV_SPECIFIC_FLAGS, direct3d11.d3d11_shader_tracking_options
ms.topic: enum
f1_keywords: 
 - "d3d11sdklayers/D3D11_SHADER_TRACKING_OPTIONS"
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
 - D3D11_SHADER_TRACKING_OPTIONS
targetos: Windows
req.typenames: D3D11_SHADER_TRACKING_OPTIONS
req.redist: 
ms.custom: 19H1
---

# D3D11_SHADER_TRACKING_OPTIONS enumeration


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
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11refdefaulttrackingoptions-settrackingoptions">ID3D11RefDefaultTrackingOptions::SetTrackingOptions</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11reftrackingoptions-settrackingoptions">ID3D11RefTrackingOptions::SetTrackingOptions</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11tracingdevice-setshadertrackingoptions">ID3D11TracingDevice::SetShaderTrackingOptions</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11tracingdevice-setshadertrackingoptionsbytype">ID3D11TracingDevice::SetShaderTrackingOptionsByType</a>
</li>
</ul>
<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.
      </div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-layer-enums">Layer Enumerations</a>
 

 

