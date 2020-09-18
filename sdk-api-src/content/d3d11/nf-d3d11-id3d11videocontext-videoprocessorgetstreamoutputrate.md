---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorGetStreamOutputRate
title: ID3D11VideoContext::VideoProcessorGetStreamOutputRate (d3d11.h)
description: Gets the rate at which the video processor produces output frames for an input stream.
helpviewer_keywords: ["FALSE","ID3D11VideoContext interface [Media Foundation]","VideoProcessorGetStreamOutputRate method","ID3D11VideoContext.VideoProcessorGetStreamOutputRate","ID3D11VideoContext::VideoProcessorGetStreamOutputRate","TRUE","VideoProcessorGetStreamOutputRate","VideoProcessorGetStreamOutputRate method [Media Foundation]","VideoProcessorGetStreamOutputRate method [Media Foundation]","ID3D11VideoContext interface","d3d11/ID3D11VideoContext::VideoProcessorGetStreamOutputRate","mf.id3d11videocontext_videoprocessorgetstreamoutputrate"]
old-location: mf\id3d11videocontext_videoprocessorgetstreamoutputrate.htm
tech.root: mf
ms.assetid: 69AC0713-FE92-4D89-857A-A0037D51B597
ms.date: 12/05/2018
ms.keywords: FALSE, ID3D11VideoContext interface [Media Foundation],VideoProcessorGetStreamOutputRate method, ID3D11VideoContext.VideoProcessorGetStreamOutputRate, ID3D11VideoContext::VideoProcessorGetStreamOutputRate, TRUE, VideoProcessorGetStreamOutputRate, VideoProcessorGetStreamOutputRate method [Media Foundation], VideoProcessorGetStreamOutputRate method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorGetStreamOutputRate, mf.id3d11videocontext_videoprocessorgetstreamoutputrate
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
 - ID3D11VideoContext::VideoProcessorGetStreamOutputRate
 - d3d11/ID3D11VideoContext::VideoProcessorGetStreamOutputRate
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
 - ID3D11VideoContext.VideoProcessorGetStreamOutputRate
---

# ID3D11VideoContext::VideoProcessorGetStreamOutputRate


## -description

Gets the rate at which the video processor produces output frames for an input stream.

## -parameters

### -param pVideoProcessor [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor">ID3D11VideoDevice::CreateVideoProcessor</a>.

### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessorenumerator-getvideoprocessorcaps">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.

### -param pOutputRate [out]

Receives a <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_output_rate">D3D11_VIDEO_PROCESSOR_OUTPUT_RATE</a> value that specifies the output rate.

### -param pRepeatFrame [out]

Receives a Boolean value that specifies how the driver performs frame-rate conversion, if required.



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

### -param pCustomRate [out]

A pointer to a <a href="/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_rational">DXGI_RATIONAL</a> structure. If the output rate is <b>D3D11_VIDEO_PROCESSOR_OUTPUT_RATE_CUSTOM</b>, the method fills in this structure with the exact output rate. Otherwise, this parameter is ignored.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>