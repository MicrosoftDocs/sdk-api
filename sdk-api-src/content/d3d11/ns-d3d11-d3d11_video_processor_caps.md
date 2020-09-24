---
UID: NS:d3d11.D3D11_VIDEO_PROCESSOR_CAPS
title: D3D11_VIDEO_PROCESSOR_CAPS (d3d11.h)
description: Describes the capabilities of a Microsoft Direct3D 11 video processor.
helpviewer_keywords: ["D3D11_VIDEO_PROCESSOR_CAPS","D3D11_VIDEO_PROCESSOR_CAPS structure [Media Foundation]","d3d11/D3D11_VIDEO_PROCESSOR_CAPS","mf.d3d11_video_processor_caps"]
old-location: mf\d3d11_video_processor_caps.htm
tech.root: mf
ms.assetid: EF79BE15-B92E-45C1-BC42-E89E06197C20
ms.date: 12/05/2018
ms.keywords: D3D11_VIDEO_PROCESSOR_CAPS, D3D11_VIDEO_PROCESSOR_CAPS structure [Media Foundation], d3d11/D3D11_VIDEO_PROCESSOR_CAPS, mf.d3d11_video_processor_caps
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
req.typenames: D3D11_VIDEO_PROCESSOR_CAPS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_VIDEO_PROCESSOR_CAPS
 - d3d11/D3D11_VIDEO_PROCESSOR_CAPS
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
 - D3D11_VIDEO_PROCESSOR_CAPS
---

# D3D11_VIDEO_PROCESSOR_CAPS structure


## -description

Describes the capabilities of a Microsoft Direct3D 11 video processor.

## -struct-fields

### -field DeviceCaps

A bitwise <b>OR</b> of zero or more flags from the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_device_caps">D3D11_VIDEO_PROCESSOR_DEVICE_CAPS</a>  enumeration.

### -field FeatureCaps

A bitwise <b>OR</b> of zero or more flags from the   <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_feature_caps">D3D11_VIDEO_PROCESSOR_FEATURE_CAPS</a> enumeration.

### -field FilterCaps

A bitwise <b>OR</b> of zero or more flags from the  <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_filter_caps">D3D11_VIDEO_PROCESSPR_FILTER_CAPS</a> enumeration.

### -field InputFormatCaps

A bitwise <b>OR</b> of zero or more flags from the  <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_format_caps">D3D11_VIDEO_PROCESSOR_FORMAT_CAPS</a> enumeration.

### -field AutoStreamCaps

A bitwise <b>OR</b> of zero or more flags from the  <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_auto_stream_caps">D3D11_VIDEO_PROCESSOR_AUTO_STREAM_CAPS</a> enumeration.

### -field StereoCaps

A bitwise <b>OR</b> of zero or more flags from the   <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_stereo_caps">D3D11_VIDEO_PROCESSOR_STEREO_CAPS</a> enumeration.

### -field RateConversionCapsCount

The number of frame-rate conversion capabilities. To enumerate the frame-rate conversion capabilities, call the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessorenumerator-getvideoprocessorrateconversioncaps">ID3D11VideoProcessorEnumerator::GetVideoProcessorRateConversionCaps</a> method.

### -field MaxInputStreams

The maximum number of input streams that can be enabled at the same time.

### -field MaxStreamStates

The maximum number of input streams for which the device can store state data.

## -remarks

The video processor stores state information for each input stream. These states persist between blits. With each blit, the application selects which streams to enable or disable. Disabling a stream does not affect the state information for that stream.

The <b>MaxStreamStates</b> member gives the maximum number of stream states that can be saved. The <b>MaxInputStreams</b> member gives the maximum number of streams that can be enabled during a blit. These two values can differ.

## -see-also

<a href="/windows/desktop/medfound/direct3d-11-video-structures">Direct3D 11 Video Structures</a>



<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessorenumerator-getvideoprocessorcaps">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a>