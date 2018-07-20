---
UID: NE:dxvahd._DXVAHD_OUTPUT_RATE
title: "_DXVAHD_OUTPUT_RATE"
author: windows-sdk-content
description: Specifies the output frame rates for an input stream, when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).
old-location: mf\dxvahd_output_rate.htm
old-project: medfound
ms.assetid: f96184d8-c5c2-4767-899f-323935fa9e89
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: DXVAHD_OUTPUT_RATE, DXVAHD_OUTPUT_RATE enumeration [Media Foundation], DXVAHD_OUTPUT_RATE_CUSTOM, DXVAHD_OUTPUT_RATE_HALF, DXVAHD_OUTPUT_RATE_NORMAL, _DXVAHD_OUTPUT_RATE, dxvahd/DXVAHD_OUTPUT_RATE, dxvahd/DXVAHD_OUTPUT_RATE_CUSTOM, dxvahd/DXVAHD_OUTPUT_RATE_HALF, dxvahd/DXVAHD_OUTPUT_RATE_NORMAL, mf.dxvahd_output_rate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: dxvahd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DXVAHD_OUTPUT_RATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxvahd.h
api_name:
 - DXVAHD_OUTPUT_RATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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
 

 

