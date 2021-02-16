---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorSetStreamAlpha
title: ID3D11VideoContext::VideoProcessorSetStreamAlpha (d3d11.h)
description: Sets the planar alpha for an input stream on the video processor.
helpviewer_keywords: ["ID3D11VideoContext interface [Media Foundation]","VideoProcessorSetStreamAlpha method","ID3D11VideoContext.VideoProcessorSetStreamAlpha","ID3D11VideoContext::VideoProcessorSetStreamAlpha","VideoProcessorSetStreamAlpha","VideoProcessorSetStreamAlpha method [Media Foundation]","VideoProcessorSetStreamAlpha method [Media Foundation]","ID3D11VideoContext interface","d3d11/ID3D11VideoContext::VideoProcessorSetStreamAlpha","mf.id3d11videocontext_videoprocessorsetstreamalpha"]
old-location: mf\id3d11videocontext_videoprocessorsetstreamalpha.htm
tech.root: mf
ms.assetid: DA869E3F-25BB-4794-B7AE-A3C2DA968800
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorSetStreamAlpha method, ID3D11VideoContext.VideoProcessorSetStreamAlpha, ID3D11VideoContext::VideoProcessorSetStreamAlpha, VideoProcessorSetStreamAlpha, VideoProcessorSetStreamAlpha method [Media Foundation], VideoProcessorSetStreamAlpha method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorSetStreamAlpha, mf.id3d11videocontext_videoprocessorsetstreamalpha
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11VideoContext::VideoProcessorSetStreamAlpha
 - d3d11/ID3D11VideoContext::VideoProcessorSetStreamAlpha
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.h
api_name:
 - ID3D11VideoContext.VideoProcessorSetStreamAlpha
---

# ID3D11VideoContext::VideoProcessorSetStreamAlpha


## -description

Sets the planar alpha for an input stream on the video processor.

## -parameters

### -param pVideoProcessor [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor">ID3D11VideoDevice::CreateVideoProcessor</a>.

### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessorenumerator-getvideoprocessorcaps">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.

### -param Enable [in]

Specifies whether alpha blending is enabled.

### -param Alpha [in]

The planar alpha value. The value can range from 0.0 (transparent) to 1.0 (opaque). 
 If <i>Enable</i> is <b>FALSE</b>, this parameter is ignored.

## -remarks

To use this feature, the driver must support stereo video, indicated by the  <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_processor_caps">D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_ALHPA_STREAM</a> capability flag. To query for this  capability, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessorenumerator-getvideoprocessorcaps">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a>.

Alpha blending is disabled by default. 
        

For each pixel, the destination color value is computed as follows:

<code>Cd = Cs * (As * Ap * Ae) + Cd * (1.0 - As * Ap * Ae)</code>

where:

<ul>
<li><code>Cd</code> = The color value of the destination pixel</li>
<li><code>Cs</code> = The color value of the source pixel</li>
<li><code>As</code> = The per-pixel source alpha</li>
<li><code>Ap</code> = The planar alpha value</li>
<li><code>Ae</code> = The palette-entry alpha value, or 1.0 (see Note)</li>
</ul>
<div class="alert"><b>Note</b>  Palette-entry alpha values apply only to palettized color formats, and only when the device supports the <b>D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_ALPHA_PALETTE</b> capability. Otherwise, this factor equals 1.0. </div>
<div> </div>
The destination alpha value is computed according to the alpha fill mode. For more information, see <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputalphafillmode">ID3D11VideoContext::VideoProcessorSetOutputAlphaFillMode</a>.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>