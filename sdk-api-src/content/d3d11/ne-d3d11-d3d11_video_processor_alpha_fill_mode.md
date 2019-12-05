---
UID: NE:d3d11.D3D11_VIDEO_PROCESSOR_ALPHA_FILL_MODE
title: D3D11_VIDEO_PROCESSOR_ALPHA_FILL_MODE (d3d11.h)
description: Specifies the alpha fill mode for video processing.
old-location: mf\d3d11_video_processor_alpha_fill_mode.htm
tech.root: medfound
ms.assetid: 185B71C5-1B27-4F7B-B842-CA04898F5DC1
ms.date: 12/05/2018
ms.keywords: D3D11_VIDEO_PROCESSOR_ALPHA_FILL_MODE, D3D11_VIDEO_PROCESSOR_ALPHA_FILL_MODE enumeration [Media Foundation], D3D11_VIDEO_PROCESSOR_ALPHA_FILL_MODE_BACKGROUND, D3D11_VIDEO_PROCESSOR_ALPHA_FILL_MODE_DESTINATION, D3D11_VIDEO_PROCESSOR_ALPHA_FILL_MODE_OPAQUE, D3D11_VIDEO_PROCESSOR_ALPHA_FILL_MODE_SOURCE_STREAM, d3d11/D3D11_VIDEO_PROCESSOR_ALPHA_FILL_MODE, d3d11/D3D11_VIDEO_PROCESSOR_ALPHA_FILL_MODE_BACKGROUND, d3d11/D3D11_VIDEO_PROCESSOR_ALPHA_FILL_MODE_DESTINATION, d3d11/D3D11_VIDEO_PROCESSOR_ALPHA_FILL_MODE_OPAQUE, d3d11/D3D11_VIDEO_PROCESSOR_ALPHA_FILL_MODE_SOURCE_STREAM, mf.d3d11_video_processor_alpha_fill_mode
ms.topic: enum
f1_keywords:
- d3d11/D3D11_VIDEO_PROCESSOR_ALPHA_FILL_MODE
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- d3d11.h
api_name:
- D3D11_VIDEO_PROCESSOR_ALPHA_FILL_MODE
targetos: Windows
req.typenames: D3D11_VIDEO_PROCESSOR_ALPHA_FILL_MODE
req.redist: 
ms.custom: 19H1
---

# D3D11_VIDEO_PROCESSOR_ALPHA_FILL_MODE enumeration


## -description


Specifies the alpha fill mode for video processing.


## -enum-fields




### -field D3D11_VIDEO_PROCESSOR_ALPHA_FILL_MODE_OPAQUE

Alpha values inside the target rectangle are set to opaque.




### -field D3D11_VIDEO_PROCESSOR_ALPHA_FILL_MODE_BACKGROUND

Alpha values inside the target rectangle are set to the alpha value specified in the background color. To set the background color, call the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputbackgroundcolor">ID3D11VideoContext::VideoProcessorSetOutputBackgroundColor</a> method.


### -field D3D11_VIDEO_PROCESSOR_ALPHA_FILL_MODE_DESTINATION

Existing alpha values remain unchanged in the output surface.


### -field D3D11_VIDEO_PROCESSOR_ALPHA_FILL_MODE_SOURCE_STREAM

Alpha values are taken from an  input stream, scaled, and copied to the corresponding destination rectangle for that stream. The input stream is specified in the <i>StreamIndex</i> parameter of the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputalphafillmode">ID3D11VideoContext::VideoProcessorSetOutputAlphaFillMode</a> method. 

If the input stream does not have alpha data, the video processor sets the alpha values in the target rectangle to opaque. If the input stream is disabled or the source rectangle is empty, the alpha values in the target rectangle are not modified.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/direct3d-11-video-enumerations">Direct3D 11 Video Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputalphafillmode">ID3D11VideoContext::VideoProcessorSetOutputAlphaFillMode</a>
 

 

