---
UID: NS:dxvahd._DXVAHD_STREAM_STATE_OUTPUT_RATE_DATA
title: DXVAHD_STREAM_STATE_OUTPUT_RATE_DATA (dxvahd.h)
description: Specifies the output frame rate for an input stream when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).
helpviewer_keywords: ["DXVAHD_STREAM_STATE_OUTPUT_RATE_DATA","DXVAHD_STREAM_STATE_OUTPUT_RATE_DATA structure [Media Foundation]","FALSE","TRUE","dxvahd/DXVAHD_STREAM_STATE_OUTPUT_RATE_DATA","mf.dxvahd_stream_state_output_rate_data"]
old-location: mf\dxvahd_stream_state_output_rate_data.htm
tech.root: mf
ms.assetid: 9cca24f0-5fff-4125-b1fe-d2f9278b5181
ms.date: 12/05/2018
ms.keywords: DXVAHD_STREAM_STATE_OUTPUT_RATE_DATA, DXVAHD_STREAM_STATE_OUTPUT_RATE_DATA structure [Media Foundation], FALSE, TRUE, dxvahd/DXVAHD_STREAM_STATE_OUTPUT_RATE_DATA, mf.dxvahd_stream_state_output_rate_data
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DXVAHD_STREAM_STATE_OUTPUT_RATE_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVAHD_STREAM_STATE_OUTPUT_RATE_DATA
 - dxvahd/_DXVAHD_STREAM_STATE_OUTPUT_RATE_DATA
 - DXVAHD_STREAM_STATE_OUTPUT_RATE_DATA
 - dxvahd/DXVAHD_STREAM_STATE_OUTPUT_RATE_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxvahd.h
api_name:
 - DXVAHD_STREAM_STATE_OUTPUT_RATE_DATA
---

# DXVAHD_STREAM_STATE_OUTPUT_RATE_DATA structure


## -description

Specifies the output frame rate for an input stream when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).

## -struct-fields

### -field RepeatFrame

Specifies how the device performs frame-rate conversion, if required. The default state value is <b>FALSE</b> (interpolation).

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
The device repeats frames.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The device interpolates frames.

</td>
</tr>
</table>

### -field OutputRate

Specifies the output rate, as a member of the <a href="/windows/desktop/api/dxvahd/ne-dxvahd-dxvahd_output_rate">DXVAHD_OUTPUT_RATE</a> enumeration.

### -field CustomRate

Specifies a custom output rate, as a <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_rational">DXVAHD_RATIONAL</a> structure. This member is ignored unless <b>OutputRate</b> equals <b>DXVAHD_OUTPUT_RATE_CUSTOM</b>. The default state value is 1/1.

To get the list of custom rates supported by the video processor, call <a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorcustomrates">IDXVAHD_Device::GetVideoProcessorCustomRates</a>. If a custom rate is used, it must be taken from this list.

## -remarks

The output rate might require the device to convert the frame rate of the input stream. If so, the value of <b>RepeatFrame</b> controls whether the device creates interpolated frames or simply repeats input frames.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/api/dxvahd/ne-dxvahd-dxvahd_stream_state">DXVAHD_STREAM_STATE</a>



<a href="/windows/desktop/medfound/direct3d-video-structures">Direct3D Video Structures</a>



<a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate">IDXVAHD_VideoProcessor::SetVideoProcessStreamState</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>