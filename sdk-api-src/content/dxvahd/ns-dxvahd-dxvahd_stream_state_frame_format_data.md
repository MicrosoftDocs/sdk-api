---
UID: NS:dxvahd._DXVAHD_STREAM_STATE_FRAME_FORMAT_DATA
title: DXVAHD_STREAM_STATE_FRAME_FORMAT_DATA (dxvahd.h)
description: Specifies how a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) input stream is interlaced.
helpviewer_keywords: ["DXVAHD_STREAM_STATE_FRAME_FORMAT_DATA","DXVAHD_STREAM_STATE_FRAME_FORMAT_DATA structure [Media Foundation]","dxvahd/DXVAHD_STREAM_STATE_FRAME_FORMAT_DATA","mf.dxvahd_stream_state_frame_format_data"]
old-location: mf\dxvahd_stream_state_frame_format_data.htm
tech.root: mf
ms.assetid: 4fa6a7f7-df9f-4e38-884c-81a01f913df0
ms.date: 12/05/2018
ms.keywords: DXVAHD_STREAM_STATE_FRAME_FORMAT_DATA, DXVAHD_STREAM_STATE_FRAME_FORMAT_DATA structure [Media Foundation], dxvahd/DXVAHD_STREAM_STATE_FRAME_FORMAT_DATA, mf.dxvahd_stream_state_frame_format_data
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
req.typenames: DXVAHD_STREAM_STATE_FRAME_FORMAT_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVAHD_STREAM_STATE_FRAME_FORMAT_DATA
 - dxvahd/_DXVAHD_STREAM_STATE_FRAME_FORMAT_DATA
 - DXVAHD_STREAM_STATE_FRAME_FORMAT_DATA
 - dxvahd/DXVAHD_STREAM_STATE_FRAME_FORMAT_DATA
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
 - DXVAHD_STREAM_STATE_FRAME_FORMAT_DATA
---

# DXVAHD_STREAM_STATE_FRAME_FORMAT_DATA structure


## -description

Specifies how a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) input stream is interlaced.

## -struct-fields

### -field FrameFormat

The video interlacing, specified as a <a href="/windows/desktop/api/dxvahd/ne-dxvahd-dxvahd_frame_format">DXVAHD_FRAME_FORMAT</a> value.

The default state value is <b>DXVAHD_FRAME_FORMAT_PROGRESSIVE</b> (progressive frames).

## -remarks

Some devices do not support interlaced RGB. Interlaced RGB support is indicated by the <b>DXVAHD_INPUT_FORMAT_CAPS_RGB_INTERLACED</b>  capability flag. If the device does not support interlaced RGB, it treats all RGB input streams as progressive frames. 

Some devices do not support interlaced formats with palettized color. This support is indicated by the <b>DXVAHD_INPUT_FORMAT_CAPS_PALETTE_INTERLACED</b> flag. If the device does not support this capability, all palettized input streams are treated as progressive frames.

To get the device's capabilities, call <a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps">IDXVAHD_Device::GetVideoProcessorDeviceCaps</a> and check the <b>InputFormatCaps</b> member of the <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps">DXVAHD_VPDEVCAPS</a> structure.


#### Examples


```cpp
HRESULT DXVAHD_SetFrameFormat(
    IDXVAHD_VideoProcessor *pVP,
    UINT stream,
    DXVAHD_FRAME_FORMAT format
    )
{
    DXVAHD_STREAM_STATE_FRAME_FORMAT_DATA frame_format = { format };

    HRESULT hr = pVP->SetVideoProcessStreamState(
        stream,
        DXVAHD_STREAM_STATE_FRAME_FORMAT,
        sizeof(frame_format),
        &frame_format
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