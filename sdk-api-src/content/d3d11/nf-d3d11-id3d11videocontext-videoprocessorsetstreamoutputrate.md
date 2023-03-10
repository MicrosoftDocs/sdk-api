---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorSetStreamOutputRate
title: ID3D11VideoContext::VideoProcessorSetStreamOutputRate (d3d11.h)
description: Sets the rate at which the video processor produces output frames for an input stream.
helpviewer_keywords: ["FALSE","ID3D11VideoContext interface [Media Foundation]","VideoProcessorSetStreamOutputRate method","ID3D11VideoContext.VideoProcessorSetStreamOutputRate","ID3D11VideoContext::VideoProcessorSetStreamOutputRate","TRUE","VideoProcessorSetStreamOutputRate","VideoProcessorSetStreamOutputRate method [Media Foundation]","VideoProcessorSetStreamOutputRate method [Media Foundation]","ID3D11VideoContext interface","d3d11/ID3D11VideoContext::VideoProcessorSetStreamOutputRate","mf.id3d11videocontext_videoprocessorsetstreamoutputrate"]
old-location: mf\id3d11videocontext_videoprocessorsetstreamoutputrate.htm
tech.root: mf
ms.assetid: D353F6E8-B465-46CB-AA47-8B097AB4AF2A
ms.date: 12/05/2018
ms.keywords: FALSE, ID3D11VideoContext interface [Media Foundation],VideoProcessorSetStreamOutputRate method, ID3D11VideoContext.VideoProcessorSetStreamOutputRate, ID3D11VideoContext::VideoProcessorSetStreamOutputRate, TRUE, VideoProcessorSetStreamOutputRate, VideoProcessorSetStreamOutputRate method [Media Foundation], VideoProcessorSetStreamOutputRate method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorSetStreamOutputRate, mf.id3d11videocontext_videoprocessorsetstreamoutputrate
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
 - ID3D11VideoContext::VideoProcessorSetStreamOutputRate
 - d3d11/ID3D11VideoContext::VideoProcessorSetStreamOutputRate
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
 - ID3D11VideoContext.VideoProcessorSetStreamOutputRate
---

# ID3D11VideoContext::VideoProcessorSetStreamOutputRate


## -description

Sets the rate at which the video processor produces output frames for an input stream.

## -parameters

### -param pVideoProcessor [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor">ID3D11VideoDevice::CreateVideoProcessor</a>.

### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessorenumerator-getvideoprocessorcaps">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.

### -param OutputRate [in]

The output rate, specified as a <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_output_rate">D3D11_VIDEO_PROCESSOR_OUTPUT_RATE</a> value.

### -param RepeatFrame [in]

Specifies how the driver performs frame-rate conversion, if required.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
Repeat frames.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Interpolate frames.

</td>
</tr>
</table>

### -param pCustomRate [in]

A pointer to a <a href="/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_rational">DXGI_RATIONAL</a> structure. If <i>OutputRate</i> is <b>D3D11_VIDEO_PROCESSOR_OUTPUT_RATE_CUSTOM</b>,  this parameter specifies the exact output rate. Otherwise, this parameter is ignored and can be <b>NULL</b>.

## -remarks

The standard output rates are normal frame-rate (<b>D3D11_VIDEO_PROCESSOR_OUTPUT_RATE_NORMAL</b>) and half frame-rate (<b>D3D11_VIDEO_PROCESSOR_OUTPUT_RATE_HALF</b>). In addition, the driver might support custom rates  for rate conversion or inverse telecine. To get the list of custom rates, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessorenumerator-getvideoprocessorcustomrate">ID3D11VideoProcessorEnumerator::GetVideoProcessorCustomRate</a>.

Depending on the output rate, the driver might need to convert the frame rate. If so, the value of <i>RepeatFrame</i> controls whether the driver creates interpolated frames or simply repeats input frames.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>