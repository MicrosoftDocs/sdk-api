---
UID: NS:dxvahd._DXVAHD_STREAM_STATE_ALPHA_DATA
title: DXVAHD_STREAM_STATE_ALPHA_DATA (dxvahd.h)
description: Specifies the planar alpha value for an input stream, when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).
helpviewer_keywords: ["DXVAHD_STREAM_STATE_ALPHA_DATA","DXVAHD_STREAM_STATE_ALPHA_DATA structure [Media Foundation]","dxvahd/DXVAHD_STREAM_STATE_ALPHA_DATA","mf.dxvahd_stream_state_alpha_data"]
old-location: mf\dxvahd_stream_state_alpha_data.htm
tech.root: mf
ms.assetid: 51135d6e-4f97-44d9-b1d5-f7d2095ee6f1
ms.date: 12/05/2018
ms.keywords: DXVAHD_STREAM_STATE_ALPHA_DATA, DXVAHD_STREAM_STATE_ALPHA_DATA structure [Media Foundation], dxvahd/DXVAHD_STREAM_STATE_ALPHA_DATA, mf.dxvahd_stream_state_alpha_data
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
req.typenames: DXVAHD_STREAM_STATE_ALPHA_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVAHD_STREAM_STATE_ALPHA_DATA
 - dxvahd/_DXVAHD_STREAM_STATE_ALPHA_DATA
 - DXVAHD_STREAM_STATE_ALPHA_DATA
 - dxvahd/DXVAHD_STREAM_STATE_ALPHA_DATA
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
 - DXVAHD_STREAM_STATE_ALPHA_DATA
---

# DXVAHD_STREAM_STATE_ALPHA_DATA structure


## -description

Specifies the planar alpha value for an input stream, when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).

## -struct-fields

### -field Enable

<b>If TRUE</b>, alpha blending is enabled. Otherwise, alpha blending is disabled. The default state value is <b>FALSE</b>.

### -field Alpha

Specifies the planar alpha value as a floating-point number from 0.0 (transparent) to 1.0 (opaque). 

If the <b>Enable</b> member is <b>FALSE</b>, this member is ignored.

## -remarks

For each pixel, the destination color value is computed as follows:

<code>Cd = Cs * (As * Ap * Ae) + Cd * (1.0 - As * Ap * Ae)</code>

where

<ul>
<li><code>Cd</code> = Color value of the destination pixel.</li>
<li><code>Cs</code> = Color value of source pixel.</li>
<li><code>As</code> = Per-pixel source alpha.</li>
<li><code>Ap</code> = Planar alpha value.</li>
<li><code>Ae</code> = Palette-entry alpha value, or 1.0 (see Note).</li>
</ul>
<div class="alert"><b>Note</b>  Palette-entry alpha values apply only to palettized color formats, and only when the device supports the <b>DXVAHD_FEATURE_CAPS_ALPHA_PALETTE</b> capability. Otherwise, this factor equals 1.0. </div>
<div> </div>
The destination alpha value is computed according to the <b>DXVAHD_BLT_STATE_ALPHA_FILL</b> state. For more information, see <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_blt_state_alpha_fill_data">DXVAHD_BLT_STATE_ALPHA_FILL_DATA</a>.

To get the device capabilities, call <a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps">IDXVAHD_Device::GetVideoProcessorDeviceCaps</a> and check the <b>FeatureCaps</b> member of the <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps">DXVAHD_VPDEVCAPS</a> structure.


#### Examples


```cpp
HRESULT DXVAHD_SetPlanarAlpha(
    IDXVAHD_VideoProcessor *pVP,
    UINT stream,
    BOOL bEnable,
    float fAlpha
    )
{
    DXVAHD_STREAM_STATE_ALPHA_DATA alpha = { bEnable, fAlpha };

    HRESULT hr = pVP->SetVideoProcessStreamState(
        stream,
        DXVAHD_STREAM_STATE_ALPHA,
        sizeof(alpha),
        &alpha
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