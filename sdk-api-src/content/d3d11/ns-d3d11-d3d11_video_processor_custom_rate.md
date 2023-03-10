---
UID: NS:d3d11.D3D11_VIDEO_PROCESSOR_CUSTOM_RATE
title: D3D11_VIDEO_PROCESSOR_CUSTOM_RATE (d3d11.h)
description: Specifies a custom rate for frame-rate conversion or inverse telecine (IVTC). (D3D11_VIDEO_PROCESSOR_CUSTOM_RATE)
helpviewer_keywords: ["D3D11_VIDEO_PROCESSOR_CUSTOM_RATE","D3D11_VIDEO_PROCESSOR_CUSTOM_RATE structure [Media Foundation]","d3d11/D3D11_VIDEO_PROCESSOR_CUSTOM_RATE","mf.d3d11_video_processor_custom_rate"]
old-location: mf\d3d11_video_processor_custom_rate.htm
tech.root: mf
ms.assetid: 237357C8-546E-41E5-8002-E5499E39DA72
ms.date: 12/05/2018
ms.keywords: D3D11_VIDEO_PROCESSOR_CUSTOM_RATE, D3D11_VIDEO_PROCESSOR_CUSTOM_RATE structure [Media Foundation], d3d11/D3D11_VIDEO_PROCESSOR_CUSTOM_RATE, mf.d3d11_video_processor_custom_rate
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
req.typenames: D3D11_VIDEO_PROCESSOR_CUSTOM_RATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_VIDEO_PROCESSOR_CUSTOM_RATE
 - d3d11/D3D11_VIDEO_PROCESSOR_CUSTOM_RATE
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
 - D3D11_VIDEO_PROCESSOR_CUSTOM_RATE
---

# D3D11_VIDEO_PROCESSOR_CUSTOM_RATE structure


## -description

Specifies a custom rate for frame-rate conversion or inverse telecine (IVTC).

## -struct-fields

### -field CustomRate

The ratio of the output frame rate to the input frame rate, expressed as a <a href="/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_rational">DXGI_RATIONAL</a> structure that holds a rational number.

### -field OutputFrames

The number of output frames that will be generated for every <i>N</i> input samples, where <i>N</i> = <b>InputFramesOrFields</b>.

### -field InputInterlaced

If <b>TRUE</b>, the input stream must be interlaced. Otherwise, the input stream must be progressive.

### -field InputFramesOrFields

The number of input fields or frames for every <i>N</i> output frames that will be generated, where <i>N</i> = <b>OutputFrames</b>.

## -remarks

The <b>CustomRate</b> member gives the rate conversion factor, while the remaining members define the pattern of input and output samples.

## -see-also

<a href="/windows/desktop/medfound/direct3d-11-video-structures">Direct3D 11 Video Structures</a>



<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessorenumerator-getvideoprocessorcustomrate">ID3D11VideoProcessorEnumerator::GetVideoProcessorCustomRate</a>
