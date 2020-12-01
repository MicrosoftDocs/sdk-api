---
UID: NS:d3d11.D3D11_VIDEO_PROCESSOR_RATE_CONVERSION_CAPS
title: D3D11_VIDEO_PROCESSOR_RATE_CONVERSION_CAPS (d3d11.h)
description: Defines a group of video processor capabilities that are associated with frame-rate conversion, including deinterlacing and inverse telecine.
helpviewer_keywords: ["D3D11_VIDEO_PROCESSOR_RATE_CONVERSION_CAPS","D3D11_VIDEO_PROCESSOR_RATE_CONVERSION_CAPS structure [Media Foundation]","d3d11/D3D11_VIDEO_PROCESSOR_RATE_CONVERSION_CAPS","mf.d3d11_video_processor_rate_conversion_caps"]
old-location: mf\d3d11_video_processor_rate_conversion_caps.htm
tech.root: mf
ms.assetid: C8C50AE4-5F4F-42AB-8FBB-37D24C4D6081
ms.date: 12/05/2018
ms.keywords: D3D11_VIDEO_PROCESSOR_RATE_CONVERSION_CAPS, D3D11_VIDEO_PROCESSOR_RATE_CONVERSION_CAPS structure [Media Foundation], d3d11/D3D11_VIDEO_PROCESSOR_RATE_CONVERSION_CAPS, mf.d3d11_video_processor_rate_conversion_caps
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.typenames: D3D11_VIDEO_PROCESSOR_RATE_CONVERSION_CAPS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_VIDEO_PROCESSOR_RATE_CONVERSION_CAPS
 - d3d11/D3D11_VIDEO_PROCESSOR_RATE_CONVERSION_CAPS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_VIDEO_PROCESSOR_RATE_CONVERSION_CAPS
---

# D3D11_VIDEO_PROCESSOR_RATE_CONVERSION_CAPS structure


## -description

Defines a group of video processor capabilities that are associated with frame-rate conversion, including deinterlacing and inverse telecine.

## -struct-fields

### -field PastFrames

The number of past reference frames required to perform the optimal video processing.

### -field FutureFrames

The number of future reference frames required to perform the optimal video processing.

### -field ProcessorCaps

A bitwise <b>OR</b> of zero or more flags from the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_processor_caps">D3D11_VIDEO_PROCESSOR_PROCESSOR_CAPS</a> enumeration.

### -field ITelecineCaps

A bitwise <b>OR</b> of zero or more flags from the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_itelecine_caps">D3D11_VIDEO_PROCESSOR_ITELECINE_CAPS</a> enumeration.

### -field CustomRateCount

The number of custom frame rates that the driver supports. To get the list of custom frame rates, call the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessorenumerator-getvideoprocessorcustomrate">ID3D11VideoProcessorEnumerator::GetVideoProcessorCustomRate</a> method.

## -see-also

<a href="/windows/desktop/medfound/direct3d-11-video-structures">Direct3D 11 Video Structures</a>