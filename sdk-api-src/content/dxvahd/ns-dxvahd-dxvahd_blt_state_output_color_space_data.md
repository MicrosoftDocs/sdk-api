---
UID: NS:dxvahd._DXVAHD_BLT_STATE_OUTPUT_COLOR_SPACE_DATA
title: DXVAHD_BLT_STATE_OUTPUT_COLOR_SPACE_DATA (dxvahd.h)
description: Specifies the output color space for blit operations, when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).
helpviewer_keywords: ["DXVAHD_BLT_STATE_OUTPUT_COLOR_SPACE_DATA","DXVAHD_BLT_STATE_OUTPUT_COLOR_SPACE_DATA structure [Media Foundation]","dxvahd/DXVAHD_BLT_STATE_OUTPUT_COLOR_SPACE_DATA","mf.dxvahd_blt_state_output_color_space_data"]
old-location: mf\dxvahd_blt_state_output_color_space_data.htm
tech.root: mf
ms.assetid: ec817ebc-dc3f-4101-863a-218f0a8c998a
ms.date: 12/05/2018
ms.keywords: DXVAHD_BLT_STATE_OUTPUT_COLOR_SPACE_DATA, DXVAHD_BLT_STATE_OUTPUT_COLOR_SPACE_DATA structure [Media Foundation], dxvahd/DXVAHD_BLT_STATE_OUTPUT_COLOR_SPACE_DATA, mf.dxvahd_blt_state_output_color_space_data
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
req.typenames: DXVAHD_BLT_STATE_OUTPUT_COLOR_SPACE_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVAHD_BLT_STATE_OUTPUT_COLOR_SPACE_DATA
 - dxvahd/_DXVAHD_BLT_STATE_OUTPUT_COLOR_SPACE_DATA
 - DXVAHD_BLT_STATE_OUTPUT_COLOR_SPACE_DATA
 - dxvahd/DXVAHD_BLT_STATE_OUTPUT_COLOR_SPACE_DATA
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
 - DXVAHD_BLT_STATE_OUTPUT_COLOR_SPACE_DATA
---

# DXVAHD_BLT_STATE_OUTPUT_COLOR_SPACE_DATA structure


## -description

Specifies the output color space for blit operations, when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).

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
Playback.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Video processing.

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
Full range (0-255).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Limited range (16-235).

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
ITU-R BT.601.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
ITU-R BT.709.

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
Conventional YCbCr.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Extended YCbCr (xvYCC).

</td>
</tr>
</table>

### -field Reserved

### -field Value

## -remarks

The <b>RGB_Range</b> member applies to RGB output, while the <b>YCbCr_Matrix</b> and <b>YCbCr_xvYCC</b> members apply to YCbCr (YUV) output. If the device performs color-space conversion on the background color, it uses the values that apply to  both color spaces.

Extended YCbCr can be used with either transfer matrix. Extended YCbCr does not change the black point or white point—the black point is still 16 and the white point is still 235. However, extended YCbCr explicitly allows blacker-than-black values in the range 1–15, and whiter-than-white values in the range 236–254. When extended YCbCr is used, the driver should not clip the luma values to the nominal 16–235 range.

If the device supports extended YCbCr, it sets the <b>DXVAHD_DEVICE_CAPS_xvYCC</b> capability flag in the <b>DeviceCaps</b>  member of the <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps">DXVAHD_VPDEVCAPS</a> structure. Otherwise, the device ignores the value of the <b>YCbCr_xvYCC</b> member and treats all YCbCr output as conventional YCbCr. To get the device's capabilities, call <a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps">IDXVAHD_Device::GetVideoProcessorDeviceCaps</a>.

If the output format is a wide-gamut RGB format, output might fall outside the nominal [0...1] range of sRGB. This is particularly true if one or more input streams use extended YCbCr.


#### Examples


```cpp
HRESULT DXVAHD_SetOutputColorSpace(
    IDXVAHD_VideoProcessor *pVP,
    BOOL bPlayback,     // TRUE = playback, FALSE = video processing
    UINT RGB_Range,     // 0 = 0-255, 1 = 16-235
    UINT YCbCr_Matrix,  // 0 = BT.601, 1 = BT.709
    UINT YCbCr_xvYCC    // 0 = Conventional YCbCr, 1 = xvYCC
    )
{
    DXVAHD_BLT_STATE_OUTPUT_COLOR_SPACE_DATA data =
    {
        bPlayback ? 0 : 1,
        RGB_Range ? 1 : 0,
        YCbCr_Matrix ? 1 : 0,
        YCbCr_xvYCC ? 1 : 0
    };

    HRESULT hr = pVP->SetVideoProcessBltState(
        DXVAHD_BLT_STATE_OUTPUT_COLOR_SPACE,
        sizeof(data),
        &data
        );

    return hr;
}

```

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/api/dxvahd/ne-dxvahd-dxvahd_blt_state">DXVAHD_BLT_STATE</a>



<a href="/windows/desktop/medfound/direct3d-video-structures">Direct3D Video Structures</a>



<a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessbltstate">IDXVAHD_VideoProcessor::SetVideoProcessBltState</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>