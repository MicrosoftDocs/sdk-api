---
UID: NS:dxvahd._DXVAHD_BLT_STATE_BACKGROUND_COLOR_DATA
title: DXVAHD_BLT_STATE_BACKGROUND_COLOR_DATA (dxvahd.h)
description: Specifies the background color for blit operations, when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).
helpviewer_keywords: ["DXVAHD_BLT_STATE_BACKGROUND_COLOR_DATA","DXVAHD_BLT_STATE_BACKGROUND_COLOR_DATA structure [Media Foundation]","dxvahd/DXVAHD_BLT_STATE_BACKGROUND_COLOR_DATA","mf.dxvahd_blt_state_background_color_data"]
old-location: mf\dxvahd_blt_state_background_color_data.htm
tech.root: mf
ms.assetid: 34b8c29e-a183-4e68-bd46-802c43d554f7
ms.date: 12/05/2018
ms.keywords: DXVAHD_BLT_STATE_BACKGROUND_COLOR_DATA, DXVAHD_BLT_STATE_BACKGROUND_COLOR_DATA structure [Media Foundation], dxvahd/DXVAHD_BLT_STATE_BACKGROUND_COLOR_DATA, mf.dxvahd_blt_state_background_color_data
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
req.typenames: DXVAHD_BLT_STATE_BACKGROUND_COLOR_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVAHD_BLT_STATE_BACKGROUND_COLOR_DATA
 - dxvahd/_DXVAHD_BLT_STATE_BACKGROUND_COLOR_DATA
 - DXVAHD_BLT_STATE_BACKGROUND_COLOR_DATA
 - dxvahd/DXVAHD_BLT_STATE_BACKGROUND_COLOR_DATA
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
 - DXVAHD_BLT_STATE_BACKGROUND_COLOR_DATA
---

# DXVAHD_BLT_STATE_BACKGROUND_COLOR_DATA structure


## -description

Specifies the background color for blit operations, when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).

## -struct-fields

### -field YCbCr

If <b>TRUE</b>, the <b>BackgroundColor</b> member specifies a YCbCr color. Otherwise, it specifies an RGB color.  The default device state is <b>FALSE</b> (RGB color).

### -field BackgroundColor

A <a href="/windows/win32/api/dxvahd/ns-dxvahd-dxvahd_color">DXVAHD_COLOR</a> union that specifies the background color. The default state value is (0.0, 0.0, 0.0, 1.0).

## -remarks

The background color is used to fill the target rectangle wherever no video image appears. Areas outside the target rectangle are not affected. See <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_blt_state_target_rect_data">DXVAHD_BLT_STATE_TARGET_RECT_DATA</a>.

The color space of the background color is determined by the color space of the output. See <a href="/windows/win32/api/dxvahd/ns-dxvahd-dxvahd_blt_state_output_color_space_data">DXVAHD_BLT_STATE_OUTPUT_COLOR_SPACE_DATA</a>.

The alpha value of the background color is used only when the alpha fill mode is <b>DXVAHD_ALPHA_FILL_MODE_BACKGROUND</b>. Otherwise, the alpha value is ignored. See <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_blt_state_alpha_fill_data">DXVAHD_BLT_STATE_ALPHA_FILL_DATA</a>.

The default background color is full-range RGB black, with opaque alpha.


#### Examples


```cpp
HRESULT DXVAHD_SetBackgroundColor(
    IDXVAHD_VideoProcessor *pVP,
    BOOL bYCbCr,
    const DXVAHD_COLOR& color
    )
{
    DXVAHD_BLT_STATE_BACKGROUND_COLOR_DATA data = { bYCbCr, color };

    HRESULT hr = pVP->SetVideoProcessBltState(
        DXVAHD_BLT_STATE_BACKGROUND_COLOR,
        sizeof (data),
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