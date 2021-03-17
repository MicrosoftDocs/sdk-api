---
UID: NS:dxvahd._DXVAHD_STREAM_STATE_PALETTE_DATA
title: DXVAHD_STREAM_STATE_PALETTE_DATA (dxvahd.h)
description: Contains the color palette entries for an input stream, when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).
helpviewer_keywords: ["DXVAHD_STREAM_STATE_PALETTE_DATA","DXVAHD_STREAM_STATE_PALETTE_DATA structure [Media Foundation]","dxvahd/DXVAHD_STREAM_STATE_PALETTE_DATA","mf.dxvahd_stream_state_palette_data"]
old-location: mf\dxvahd_stream_state_palette_data.htm
tech.root: mf
ms.assetid: 91f69451-72e6-4028-92d5-555dcf834cf7
ms.date: 12/05/2018
ms.keywords: DXVAHD_STREAM_STATE_PALETTE_DATA, DXVAHD_STREAM_STATE_PALETTE_DATA structure [Media Foundation], dxvahd/DXVAHD_STREAM_STATE_PALETTE_DATA, mf.dxvahd_stream_state_palette_data
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
req.typenames: DXVAHD_STREAM_STATE_PALETTE_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVAHD_STREAM_STATE_PALETTE_DATA
 - dxvahd/_DXVAHD_STREAM_STATE_PALETTE_DATA
 - DXVAHD_STREAM_STATE_PALETTE_DATA
 - dxvahd/DXVAHD_STREAM_STATE_PALETTE_DATA
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
 - DXVAHD_STREAM_STATE_PALETTE_DATA
---

# DXVAHD_STREAM_STATE_PALETTE_DATA structure


## -description

Contains the color palette entries for an input stream, when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).

## -struct-fields

### -field Count

The number of palette entries. The default state value is 0.

### -field pEntries

A pointer to an array of <b>D3DCOLOR</b> values. For RGB streams, the palette entries use a D3DFMT_A8R8G8B8 (ARGB-32) representation. For YCbCr streams, the palette entries use an AYUV representation. The alpha channel is used for alpha blending; see <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_stream_state_alpha_data">DXVAHD_STREAM_STATE_ALPHA_DATA</a>.

## -remarks

This stream state is used for input streams that have a palettized color format. Palettized formats with 4 bits per pixel (bpp) use the first 16 entries in the list. Formats with 8 bpp use the first 256 entries.

If a pixel has a palette index greater than the number of entries, the device treats the pixel as being white with opaque alpha. For full-range RGB, this value will be (255, 255, 255, 255); for YCbCr the value will be (255, 235, 128, 128).

The caller allocates the <b>pEntries</b> array. Set the <b>Count</b> member to the number of elements in the array. When retrieving the state data, you can set the <b>pEntries</b> member to <b>NULL</b> to get the number of palette entries. The device will return the count in the <b>Count</b> member.

If the DXVA-HD device does not have the <b>DXVAHD_FEATURE_CAPS_ALPHA_PALETTE</b> capability, every palette entry must have an alpha value of 0xFF (opaque). Otherwise, an error is returned from <a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate">IDXVAHD_VideoProcessor::SetVideoProcessStreamState</a>. 

To get the device capabilities, call <a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps">IDXVAHD_Device::GetVideoProcessorDeviceCaps</a> and check the <b>FeatureCaps</b> member of the <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps">DXVAHD_VPDEVCAPS</a> structure.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/api/dxvahd/ne-dxvahd-dxvahd_stream_state">DXVAHD_STREAM_STATE</a>



<a href="/windows/desktop/medfound/direct3d-video-structures">Direct3D Video Structures</a>



<a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate">IDXVAHD_VideoProcessor::SetVideoProcessStreamState</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>