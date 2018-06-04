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

# _DXVAHD_OUTPUT_RATE enumeration


## -description


Specifies the output frame rates for an input stream, when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).

This enumeration type is used in the <a href="https://msdn.microsoft.com/9cca24f0-5fff-4125-b1fe-d2f9278b5181">DXVAHD_STREAM_STATE_OUTPUT_RATE_DATA</a> structure.


## -enum-fields




### -field DXVAHD_OUTPUT_RATE_NORMAL

The frame output is at the normal rate.

For progressive input, every frame produces one output frame. For interlaced input, every frame (two fields) produces two progressive output frames.


### -field DXVAHD_OUTPUT_RATE_HALF

The frame output is at half rate.

For progressive input, every frame produces one output frame, just as with  <b>DXVAHD_OUTPUT_RATE_NORMAL</b>. For interlaced input, every frame produces one progressive output frame.


### -field DXVAHD_OUTPUT_RATE_CUSTOM

Frame output is at a custom rate.

 Use this value for frame-rate conversion or inverse telecine. The exact rate is given in the <b>OutputRate</b> member of the <a href="https://msdn.microsoft.com/9cca24f0-5fff-4125-b1fe-d2f9278b5181">DXVAHD_STREAM_STATE_OUTPUT_RATE_DATA</a> structure. To get the list of custom rates supported by the video processor, call the <a href="https://msdn.microsoft.com/63e835bb-dda2-4449-8474-219a373da82d">IDXVAHD_Device::GetVideoProcessorCustomRates</a> method.


## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/9cca24f0-5fff-4125-b1fe-d2f9278b5181">DXVAHD_STREAM_STATE_OUTPUT_RATE_DATA</a>



<a href="https://msdn.microsoft.com/41959498-501d-4f0d-ba1f-1c0690b62f4d">Direct3D Video Enumerations</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

