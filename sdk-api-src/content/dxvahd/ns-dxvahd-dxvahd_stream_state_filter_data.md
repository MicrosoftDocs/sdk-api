---
UID: NS:dxvahd._DXVAHD_STREAM_STATE_FILTER_DATA
title: DXVAHD_STREAM_STATE_FILTER_DATA (dxvahd.h)
description: Specifies the level for a filtering operation on a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) input stream.
helpviewer_keywords: ["DXVAHD_STREAM_STATE_FILTER_DATA","DXVAHD_STREAM_STATE_FILTER_DATA structure [Media Foundation]","dxvahd/DXVAHD_STREAM_STATE_FILTER_DATA","mf.dxvahd_stream_state_filter_data"]
old-location: mf\dxvahd_stream_state_filter_data.htm
tech.root: mf
ms.assetid: 2f70222d-f87a-49a5-8da5-15dfa2807cd7
ms.date: 12/05/2018
ms.keywords: DXVAHD_STREAM_STATE_FILTER_DATA, DXVAHD_STREAM_STATE_FILTER_DATA structure [Media Foundation], dxvahd/DXVAHD_STREAM_STATE_FILTER_DATA, mf.dxvahd_stream_state_filter_data
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
req.typenames: DXVAHD_STREAM_STATE_FILTER_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVAHD_STREAM_STATE_FILTER_DATA
 - dxvahd/_DXVAHD_STREAM_STATE_FILTER_DATA
 - DXVAHD_STREAM_STATE_FILTER_DATA
 - dxvahd/DXVAHD_STREAM_STATE_FILTER_DATA
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
 - DXVAHD_STREAM_STATE_FILTER_DATA
---

# DXVAHD_STREAM_STATE_FILTER_DATA structure


## -description

Specifies the level for a filtering operation on a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) input stream.

## -struct-fields

### -field Enable

<b>If TRUE</b>, the filter is enabled. Otherwise, <b>the filter is disabled</b>.

### -field Level

The level for the filter. The meaning of this value depends on the implementation. To get the range and default value of a particular filter, call the <a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorfilterrange">IDXVAHD_Device::GetVideoProcessorFilterRange</a> method.

If the <b>Enable</b> member is <b>FALSE</b>, the <b>Level</b> member is ignored.

## -remarks

For a list of image filters that are defined for DXVA-HD, see <a href="/windows/desktop/api/dxvahd/ne-dxvahd-dxvahd_filter">DXVAHD_FILTER</a>. The device might not support every type of image filter. To find out whether the device supports a particular filter, call the <a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps">IDXVAHD_Device::GetVideoProcessorDeviceCaps</a> method and check the <b>FilterCaps</b> member of the <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps">DXVAHD_VPDEVCAPS</a> structure.


#### Examples


```cpp
HRESULT DXVAHD_SetFilterValue(
    IDXVAHD_VideoProcessor *pVP,
    UINT stream,
    DXVAHD_FILTER filter,
    BOOL bEnable,
    INT value
    )
{
    DXVAHD_STREAM_STATE_FILTER_DATA data = { bEnable, value };

    DXVAHD_STREAM_STATE state = static_cast<DXVAHD_STREAM_STATE>(DXVAHD_STREAM_STATE_FILTER_BRIGHTNESS + filter);

    HRESULT hr = pVP->SetVideoProcessStreamState(
        stream,
        state,
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