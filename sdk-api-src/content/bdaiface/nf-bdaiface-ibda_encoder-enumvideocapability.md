---
UID: NF:bdaiface.IBDA_Encoder.EnumVideoCapability
title: IBDA_Encoder::EnumVideoCapability (bdaiface.h)
description: Gets one of the video formats supported by the device.
helpviewer_keywords: ["EnumVideoCapability","EnumVideoCapability method [Microsoft TV Technologies]","EnumVideoCapability method [Microsoft TV Technologies]","IBDA_Encoder interface","IBDA_Encoder interface [Microsoft TV Technologies]","EnumVideoCapability method","IBDA_Encoder.EnumVideoCapability","IBDA_Encoder::EnumVideoCapability","PBDA_Encoder_Video_AVC","PBDA_Encoder_Video_H264","PBDA_Encoder_Video_MPEG2PartII","PBDA_Encoder_Video_MPEG4Part10","bdaiface/IBDA_Encoder::EnumVideoCapability","mstv.ibda_encoder_enumvideocapability"]
old-location: mstv\ibda_encoder_enumvideocapability.htm
tech.root: mstv
ms.assetid: 81a780d3-1b1c-4c9a-9b4b-cb82f83fb7d6
ms.date: 12/05/2018
ms.keywords: EnumVideoCapability, EnumVideoCapability method [Microsoft TV Technologies], EnumVideoCapability method [Microsoft TV Technologies],IBDA_Encoder interface, IBDA_Encoder interface [Microsoft TV Technologies],EnumVideoCapability method, IBDA_Encoder.EnumVideoCapability, IBDA_Encoder::EnumVideoCapability, PBDA_Encoder_Video_AVC, PBDA_Encoder_Video_H264, PBDA_Encoder_Video_MPEG2PartII, PBDA_Encoder_Video_MPEG4Part10, bdaiface/IBDA_Encoder::EnumVideoCapability, mstv.ibda_encoder_enumvideocapability
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bdaiface.idl
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
 - IBDA_Encoder::EnumVideoCapability
 - bdaiface/IBDA_Encoder::EnumVideoCapability
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_Encoder.EnumVideoCapability
---

# IBDA_Encoder::EnumVideoCapability


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets one of the video formats supported by the device.

## -parameters

### -param FmtIndex [in]

The zero-based index of the video format to retrieve. To get the number of video formats, call <a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_encoder-querycapabilities">IBDA_Encoder::QueryCapabilities</a>.

### -param MethodID [out]

Receives a value that uniquely identifies this video method.

### -param AlgorithmType [out]

Receives the type of encoding algorithm. The following values are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PBDA_Encoder_Video_MPEG2PartII"></a><a id="pbda_encoder_video_mpeg2partii"></a><a id="PBDA_ENCODER_VIDEO_MPEG2PARTII"></a><dl>
<dt><b>PBDA_Encoder_Video_MPEG2PartII</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
MPEG-2, Part 2.

</td>
</tr>
<tr>
<td width="40%"><a id="PBDA_Encoder_Video_MPEG4Part10"></a><a id="pbda_encoder_video_mpeg4part10"></a><a id="PBDA_ENCODER_VIDEO_MPEG4PART10"></a><dl>
<dt><b>PBDA_Encoder_Video_MPEG4Part10</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
MPEG-4, Part 10.

</td>
</tr>
<tr>
<td width="40%"><a id="PBDA_Encoder_Video_AVC"></a><a id="pbda_encoder_video_avc"></a><a id="PBDA_ENCODER_VIDEO_AVC"></a><dl>
<dt><b>PBDA_Encoder_Video_AVC</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
AVC video.

</td>
</tr>
<tr>
<td width="40%"><a id="PBDA_Encoder_Video_H264"></a><a id="pbda_encoder_video_h264"></a><a id="PBDA_ENCODER_VIDEO_H264"></a><dl>
<dt><b>PBDA_Encoder_Video_H264</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
H.264 video.

</td>
</tr>
</table>

### -param VerticalSize [out]

Receives the vertical_size_value field.

### -param HorizontalSize [out]

Receives the horizontal_size_value field.

### -param AspectRatio [out]

Receives the aspect_ratio_information field.

### -param FrameRateCode [out]

Receives the frame_rate_code field.

### -param ProgressiveSequence [out]

Receives the progressive_sequence field.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <i>VerticalSize</i>, <i>HorizontalSize</i>, <i>AspectRatio</i>, <i>FrameRateCode</i>, and <i>ProgressiveSequence</i> parameters are interpreted according to the ANSI/SCTE 43 2005 standard.

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_encoder">IBDA_Encoder</a>