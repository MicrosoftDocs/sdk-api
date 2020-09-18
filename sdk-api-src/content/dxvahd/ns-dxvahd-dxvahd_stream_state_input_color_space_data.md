---
UID: NS:dxvahd._DXVAHD_STREAM_STATE_INPUT_COLOR_SPACE_DATA
title: DXVAHD_STREAM_STATE_INPUT_COLOR_SPACE_DATA (dxvahd.h)
description: Specifies the color space for a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) input stream.
helpviewer_keywords: ["DXVAHD_STREAM_STATE_INPUT_COLOR_SPACE_DATA","DXVAHD_STREAM_STATE_INPUT_COLOR_SPACE_DATA structure [Media Foundation]","dxvahd/DXVAHD_STREAM_STATE_INPUT_COLOR_SPACE_DATA","mf.dxvahd_stream_state_input_color_space_data"]
old-location: mf\dxvahd_stream_state_input_color_space_data.htm
tech.root: mf
ms.assetid: 54b53e4d-990b-4496-aae6-039f443337ae
ms.date: 12/05/2018
ms.keywords: DXVAHD_STREAM_STATE_INPUT_COLOR_SPACE_DATA, DXVAHD_STREAM_STATE_INPUT_COLOR_SPACE_DATA structure [Media Foundation], dxvahd/DXVAHD_STREAM_STATE_INPUT_COLOR_SPACE_DATA, mf.dxvahd_stream_state_input_color_space_data
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
req.typenames: DXVAHD_STREAM_STATE_INPUT_COLOR_SPACE_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVAHD_STREAM_STATE_INPUT_COLOR_SPACE_DATA
 - dxvahd/_DXVAHD_STREAM_STATE_INPUT_COLOR_SPACE_DATA
 - DXVAHD_STREAM_STATE_INPUT_COLOR_SPACE_DATA
 - dxvahd/DXVAHD_STREAM_STATE_INPUT_COLOR_SPACE_DATA
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
 - DXVAHD_STREAM_STATE_INPUT_COLOR_SPACE_DATA
---

# DXVAHD_STREAM_STATE_INPUT_COLOR_SPACE_DATA structure


## -description

Specifies the color space for a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) input stream.

## -struct-fields

### -field Type

Specifies whether the input stream contains video or graphics. The device can optimize the processing based on the type. The default state value is 0 (video).

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
Video.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Graphics.

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

Specifies whether the input stream uses conventional YCbCr or extended YCbCr (xvYCC). The default state value is 0 (conventional YCbCr).

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

The <b>RGB_Range</b> member applies to RGB input, while the <b>YCbCr_Matrix</b> and <b>YCbCr_xvYCC</b> members apply to YCbCr (YUV) input.

In some situations, the device might perform an intermediate color conversion on the input stream. If so, it uses the flags that apply to  both color spaces. For example, suppose the device converts from RGB to YCbCr. If the <b>RGB_Range</b> member is 0 and the <b>YCbCr_Matrix</b> member is 1, the device will convert from full-range RGB to BT.709 YCbCr.

If the device supports xvYCC, it returns the <b>DXVAHD_DEVICE_CAPS_xvYCC</b> capability flag in the <b>DeviceCaps</b>  member of the <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps">DXVAHD_VPDEVCAPS</a> structure. Otherwise, the device ignores the value of <b>YCbCr_xvYCC</b> and treats all YCbCr input as conventional YCbCr. To get the device's capabilities, call <a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps">IDXVAHD_Device::GetVideoProcessorDeviceCaps</a>.


#### Examples


```cpp
HRESULT DXVAHD_SetInputColorSpace(
    IDXVAHD_VideoProcessor *pVP,
    UINT stream,
    BOOL bPlayback,     // TRUE = playback, FALSE = video processing
    UINT RGB_Range,     // 0 = 0-255, 1 = 16-235
    UINT YCbCr_Matrix,  // 0 = BT.601, 1 = BT.709
    UINT YCbCr_xvYCC    // 0 = Conventional YCbCr, 1 = xvYCC
    )
{
    DXVAHD_STREAM_STATE_INPUT_COLOR_SPACE_DATA data =
    {
        bPlayback ? 0 : 1,
        RGB_Range ? 1 : 0,
        YCbCr_Matrix ? 1 : 0,
        YCbCr_xvYCC ? 1 : 0
    };

    HRESULT hr = pVP->SetVideoProcessStreamState(
        stream,
        DXVAHD_STREAM_STATE_INPUT_COLOR_SPACE,
        sizeof(data),
        &data
        );

    return hr;
}

```

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/api/dxvahd/ne-dxvahd-dxvahd_stream_state">DXVAHD_STREAM_STATE</a>



<a href="/windows/desktop/medfound/direct3d-video-structures">Direct3D Video Structures</a>



<a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate">IDXVAHD_VideoProcessor::SetVideoProcessStreamState</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>