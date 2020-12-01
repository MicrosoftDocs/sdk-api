---
UID: NS:d3d11.D3D11_VIDEO_PROCESSOR_COLOR_SPACE
title: D3D11_VIDEO_PROCESSOR_COLOR_SPACE (d3d11.h)
description: Specifies the color space for video processing.
helpviewer_keywords: ["D3D11_VIDEO_PROCESSOR_COLOR_SPACE","D3D11_VIDEO_PROCESSOR_COLOR_SPACE structure [Media Foundation]","d3d11/D3D11_VIDEO_PROCESSOR_COLOR_SPACE","mf.d3d11_video_processor_color_space"]
old-location: mf\d3d11_video_processor_color_space.htm
tech.root: mf
ms.assetid: D5F36CFC-ED36-47F3-A07A-9B163F904D74
ms.date: 12/05/2018
ms.keywords: D3D11_VIDEO_PROCESSOR_COLOR_SPACE, D3D11_VIDEO_PROCESSOR_COLOR_SPACE structure [Media Foundation], d3d11/D3D11_VIDEO_PROCESSOR_COLOR_SPACE, mf.d3d11_video_processor_color_space
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
req.typenames: D3D11_VIDEO_PROCESSOR_COLOR_SPACE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_VIDEO_PROCESSOR_COLOR_SPACE
 - d3d11/D3D11_VIDEO_PROCESSOR_COLOR_SPACE
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
 - D3D11_VIDEO_PROCESSOR_COLOR_SPACE
---

# D3D11_VIDEO_PROCESSOR_COLOR_SPACE structure


## -description

Specifies the color space for video processing.

## -struct-fields

### -field Usage

Specifies whether the output is intended for playback or video processing (such as editing or authoring). The device can optimize the processing based on the type. The default state value is 0 (playback). 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Playback

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Video processing

</td>
</tr>
</table>

### -field RGB_Range

Specifies the RGB color range. The default state value is 0 (full range).



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Full range (0-255)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Limited range (16-235)

</td>
</tr>
</table>

### -field YCbCr_Matrix

Specifies the YCbCr transfer matrix. The default state value is 0 (BT.601).



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
ITU-R BT.601

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
ITU-R BT.709

</td>
</tr>
</table>

### -field YCbCr_xvYCC

Specifies whether the output uses conventional YCbCr or extended YCbCr (xvYCC). The default state value is zero (conventional YCbCr).



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Conventional YCbCr

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Extended YCbCr (xvYCC)

</td>
</tr>
</table>

### -field Nominal_Range

Specifies the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_nominal_range">D3D11_VIDEO_PROCESSOR_NOMINAL_RANGE</a>.



Introduced in Windows 8.1.

### -field Reserved

Reserved. Set to zero.

## -remarks

The <b>RGB_Range</b> member applies to RGB output, while the <b>YCbCr_Matrix</b> and <b>YCbCr_xvYCC</b> members apply to YCbCr output. If the driver performs color-space conversion on the background color, it uses the values that apply to both color spaces.



If the driver supports extended YCbCr (xvYCC), it returns the <b>D3D11_VIDEO_PROCESSOR_DEVICE_CAPS_xvYCC</b> capabilities flag in the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessorenumerator-getvideoprocessorcaps">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> method. Otherwise, the driver ignores the value of <b>YCbCr_xvYCC</b> and treats all YCbCr output as conventional YCbCr. 

If extended YCbCr is supported, it can be used with either transfer matrix. Extended YCbCr does not change the black point or white point—the black point is still 16 and the white point is still 235. However, extended YCbCr explicitly allows blacker-than-black values in the range 1–15, and whiter-than-white values in the range 236–254. When extended YCbCr is used, the driver should not clip the luma values to the nominal 16–235 range.

## -see-also

<a href="/windows/desktop/medfound/direct3d-11-video-structures">Direct3D 11 Video Structures</a>