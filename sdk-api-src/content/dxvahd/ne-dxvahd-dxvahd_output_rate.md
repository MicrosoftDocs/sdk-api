---
UID: NE:dxvahd._DXVAHD_OUTPUT_RATE
title: DXVAHD_OUTPUT_RATE (dxvahd.h)
description: Specifies the output frame rates for an input stream, when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).
helpviewer_keywords: ["DXVAHD_OUTPUT_RATE","DXVAHD_OUTPUT_RATE enumeration [Media Foundation]","DXVAHD_OUTPUT_RATE_CUSTOM","DXVAHD_OUTPUT_RATE_HALF","DXVAHD_OUTPUT_RATE_NORMAL","dxvahd/DXVAHD_OUTPUT_RATE","dxvahd/DXVAHD_OUTPUT_RATE_CUSTOM","dxvahd/DXVAHD_OUTPUT_RATE_HALF","dxvahd/DXVAHD_OUTPUT_RATE_NORMAL","mf.dxvahd_output_rate"]
old-location: mf\dxvahd_output_rate.htm
tech.root: mf
ms.assetid: f96184d8-c5c2-4767-899f-323935fa9e89
ms.date: 12/05/2018
ms.keywords: DXVAHD_OUTPUT_RATE, DXVAHD_OUTPUT_RATE enumeration [Media Foundation], DXVAHD_OUTPUT_RATE_CUSTOM, DXVAHD_OUTPUT_RATE_HALF, DXVAHD_OUTPUT_RATE_NORMAL, dxvahd/DXVAHD_OUTPUT_RATE, dxvahd/DXVAHD_OUTPUT_RATE_CUSTOM, dxvahd/DXVAHD_OUTPUT_RATE_HALF, dxvahd/DXVAHD_OUTPUT_RATE_NORMAL, mf.dxvahd_output_rate
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
req.typenames: DXVAHD_OUTPUT_RATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVAHD_OUTPUT_RATE
 - dxvahd/_DXVAHD_OUTPUT_RATE
 - DXVAHD_OUTPUT_RATE
 - dxvahd/DXVAHD_OUTPUT_RATE
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
 - DXVAHD_OUTPUT_RATE
---

# DXVAHD_OUTPUT_RATE enumeration


## -description

Specifies the output frame rates for an input stream, when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).

This enumeration type is used in the <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_stream_state_output_rate_data">DXVAHD_STREAM_STATE_OUTPUT_RATE_DATA</a> structure.

## -enum-fields

### -field DXVAHD_OUTPUT_RATE_NORMAL:0

The frame output is at the normal rate.

For progressive input, every frame produces one output frame. For interlaced input, every frame (two fields) produces two progressive output frames.

### -field DXVAHD_OUTPUT_RATE_HALF:1

The frame output is at half rate.

For progressive input, every frame produces one output frame, just as with  <b>DXVAHD_OUTPUT_RATE_NORMAL</b>. For interlaced input, every frame produces one progressive output frame.

### -field DXVAHD_OUTPUT_RATE_CUSTOM:2

Frame output is at a custom rate.

 Use this value for frame-rate conversion or inverse telecine. The exact rate is given in the <b>OutputRate</b> member of the <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_stream_state_output_rate_data">DXVAHD_STREAM_STATE_OUTPUT_RATE_DATA</a> structure. To get the list of custom rates supported by the video processor, call the <a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorcustomrates">IDXVAHD_Device::GetVideoProcessorCustomRates</a> method.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_stream_state_output_rate_data">DXVAHD_STREAM_STATE_OUTPUT_RATE_DATA</a>



<a href="/windows/desktop/medfound/direct3d-video-enumerations">Direct3D Video Enumerations</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
