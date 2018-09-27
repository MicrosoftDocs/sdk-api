---
UID: NS:dxvahd._DXVAHD_BLT_STATE_BACKGROUND_COLOR_DATA
title: "_DXVAHD_BLT_STATE_BACKGROUND_COLOR_DATA"
author: windows-sdk-content
description: Specifies the background color for blit operations, when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).
old-location: mf\dxvahd_blt_state_background_color_data.htm
tech.root: medfound
ms.assetid: 34b8c29e-a183-4e68-bd46-802c43d554f7
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: DXVAHD_BLT_STATE_BACKGROUND_COLOR_DATA, DXVAHD_BLT_STATE_BACKGROUND_COLOR_DATA structure [Media Foundation], _DXVAHD_BLT_STATE_BACKGROUND_COLOR_DATA, dxvahd/DXVAHD_BLT_STATE_BACKGROUND_COLOR_DATA, mf.dxvahd_blt_state_background_color_data
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxvahd.h
api_name:
 - DXVAHD_BLT_STATE_BACKGROUND_COLOR_DATA
product: Windows
targetos: Windows
req.typenames: DXVAHD_BLT_STATE_BACKGROUND_COLOR_DATA
req.redist: 
---

# _DXVAHD_BLT_STATE_BACKGROUND_COLOR_DATA structure


## -description


Specifies the background color for blit operations, when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).


## -struct-fields




### -field YCbCr

If <b>TRUE</b>, the <b>BackgroundColor</b> member specifies a YCbCr color. Otherwise, it specifies an RGB color.  The default device state is <b>FALSE</b> (RGB color).


### -field BackgroundColor

A <a href="https://msdn.microsoft.com/833bb91b-d891-4c3f-be20-367b0a23e97e">DXVAHD_COLOR</a> union that specifies the background color. The default state value is (0.0, 0.0, 0.0, 1.0).


## -remarks



The background color is used to fill the target rectangle wherever no video image appears. Areas outside the target rectangle are not affected. See <a href="https://msdn.microsoft.com/2a810071-b5f7-4216-8108-83dce5c12836">DXVAHD_BLT_STATE_TARGET_RECT_DATA</a>.

The color space of the background color is determined by the color space of the output. See <a href="https://msdn.microsoft.com/ec817ebc-dc3f-4101-863a-218f0a8c998a">DXVAHD_BLT_STATE_OUTPUT_COLOR_SPACE_DATA</a>.

The alpha value of the background color is used only when the alpha fill mode is <b>DXVAHD_ALPHA_FILL_MODE_BACKGROUND</b>. Otherwise, the alpha value is ignored. See <a href="https://msdn.microsoft.com/dcd42210-d5f8-42c7-aac0-08f0ce4b7ac9">DXVAHD_BLT_STATE_ALPHA_FILL_DATA</a>.

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




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/cd5f56ff-61d7-49df-8114-f6a14de8e06b">DXVAHD_BLT_STATE</a>



<a href="https://msdn.microsoft.com/584c087e-53f0-42d8-99ed-a0d013379363">Direct3D Video Structures</a>



<a href="https://msdn.microsoft.com/adc08662-7977-402d-9eb1-505333550fc8">IDXVAHD_VideoProcessor::SetVideoProcessBltState</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

