---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IBDA_Encoder::EnumVideoCapability


## -description


Gets one of the video formats supported by the device.


## -parameters




### -param FmtIndex [in]

The zero-based index of the video format to retrieve. To get the number of video formats, call <a href="https://msdn.microsoft.com/038f9360-0515-4655-9397-cd1bfb6c3d21">IBDA_Encoder::QueryCapabilities</a>.


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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <i>VerticalSize</i>, <i>HorizontalSize</i>, <i>AspectRatio</i>, <i>FrameRateCode</i>, and <i>ProgressiveSequence</i> parameters are interpreted according to the ANSI/SCTE 43 2005 standard.




## -see-also




<a href="https://msdn.microsoft.com/43ed9d91-c769-4fb3-bcd9-e5239ec5d9c7">IBDA_Encoder</a>
 

 

