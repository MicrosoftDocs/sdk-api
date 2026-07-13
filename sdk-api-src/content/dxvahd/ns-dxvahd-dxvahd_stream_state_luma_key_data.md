---
UID: NS:dxvahd._DXVAHD_STREAM_STATE_LUMA_KEY_DATA
title: DXVAHD_STREAM_STATE_LUMA_KEY_DATA (dxvahd.h)
description: Specifies the luma key for an input stream, when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).
helpviewer_keywords: ["DXVAHD_STREAM_STATE_LUMA_KEY_DATA","DXVAHD_STREAM_STATE_LUMA_KEY_DATA structure [Media Foundation]","dxvahd/DXVAHD_STREAM_STATE_LUMA_KEY_DATA","mf.dxvahd_stream_state_luma_key_data"]
old-location: mf\dxvahd_stream_state_luma_key_data.htm
tech.root: mf
ms.assetid: d94b04d9-9d94-4392-a0bf-a33210aeef1f
ms.date: 12/05/2018
ms.keywords: DXVAHD_STREAM_STATE_LUMA_KEY_DATA, DXVAHD_STREAM_STATE_LUMA_KEY_DATA structure [Media Foundation], dxvahd/DXVAHD_STREAM_STATE_LUMA_KEY_DATA, mf.dxvahd_stream_state_luma_key_data
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
req.typenames: DXVAHD_STREAM_STATE_LUMA_KEY_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVAHD_STREAM_STATE_LUMA_KEY_DATA
 - dxvahd/_DXVAHD_STREAM_STATE_LUMA_KEY_DATA
 - DXVAHD_STREAM_STATE_LUMA_KEY_DATA
 - dxvahd/DXVAHD_STREAM_STATE_LUMA_KEY_DATA
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
 - DXVAHD_STREAM_STATE_LUMA_KEY_DATA
---

# DXVAHD_STREAM_STATE_LUMA_KEY_DATA structure


## -description

Specifies the luma key for an input stream, when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).

## -struct-fields

### -field Enable

If <b>TRUE</b>, luma keying is enabled. Otherwise, luma keying is disabled. The default value is <b>FALSE</b>.

### -field Lower

The lower bound for the luma key. The range is [0…1]. The default state value is 0.0.

### -field Upper

The upper bound for the luma key. The range is [0…1]. The default state value is 0.0.

## -remarks

To use this state, the device must support luma keying, indicated by the <b>DXVAHD_FEATURE_CAPS_LUMA_KEY</b> capability flag. To query for this capability, call <a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps">IDXVAHD_Device::GetVideoProcessorDeviceCaps</a>. If the device supports luma keying, it sets the  <b>DXVAHD_FEATURE_CAPS_LUMA_KEY</b> flag in the <b>FeatureCaps</b> member of the <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps">DXVAHD_VPDEVCAPS</a> structure.

If the device does not support luma keying, the <a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate">IDXVAHD_VideoProcessor::SetVideoProcessStreamState</a> method fails for this state.

If the input format is RGB, the device must also support the <b>DXVAHD_INPUT_FORMAT_CAPS_RGB_LUMA_KEY</b> capability. This capability flag is set in the <b>InputFormatCaps</b> member of the <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps">DXVAHD_VPDEVCAPS</a> structure. If the flag is not present, the device ignores the luma key value for RGB input.

The values of <b>Lower</b> and <b>Upper</b> give the lower and upper bounds of the luma key, using a nominal range of [0...1]. Given a format with <i>n</i> bits per channel, these values are converted to luma values as follows:

<code>val = f * ((1 &lt;&lt; n)-1)</code>

Any pixel whose luma value falls within the upper and lower bounds (inclusive) is treated as transparent.

For example, if the pixel format uses 8-bit luma, the upper bound is calculated as follows:

<code>BYTE Y = BYTE(max(min(1.0, Upper), 0.0) * 255.0)</code>

Note that the value is clamped to the range [0...1] before multiplying by 255.


#### Examples


```cpp
HRESULT DXVAHD_SetLumaKey(
    IDXVAHD_VideoProcessor *pVP,
    UINT stream,
    BOOL bEnable,
    float fLower,   // Lower bound for the luma key.
    float fUpper    // Upper bound for the luma key.
    )
{
    DXVAHD_STREAM_STATE_LUMA_KEY_DATA luma = { bEnable, fLower, fUpper };

    HRESULT hr = pVP->SetVideoProcessStreamState(
        stream,
        DXVAHD_STREAM_STATE_LUMA_KEY,
        sizeof(luma),
        &luma
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