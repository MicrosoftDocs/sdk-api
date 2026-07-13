---
UID: NE:dxvahd._DXVAHD_PROCESSOR_CAPS
title: DXVAHD_PROCESSOR_CAPS (dxvahd.h)
description: Specifies the processing capabilities of a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.
helpviewer_keywords: ["DXVAHD_PROCESSOR_CAPS","DXVAHD_PROCESSOR_CAPS enumeration [Media Foundation]","DXVAHD_PROCESSOR_CAPS_DEINTERLACE_ADAPTIVE","DXVAHD_PROCESSOR_CAPS_DEINTERLACE_BLEND","DXVAHD_PROCESSOR_CAPS_DEINTERLACE_BOB","DXVAHD_PROCESSOR_CAPS_DEINTERLACE_MOTION_COMPENSATION","DXVAHD_PROCESSOR_CAPS_FRAME_RATE_CONVERSION","DXVAHD_PROCESSOR_CAPS_INVERSE_TELECINE","dxvahd/DXVAHD_PROCESSOR_CAPS","dxvahd/DXVAHD_PROCESSOR_CAPS_DEINTERLACE_ADAPTIVE","dxvahd/DXVAHD_PROCESSOR_CAPS_DEINTERLACE_BLEND","dxvahd/DXVAHD_PROCESSOR_CAPS_DEINTERLACE_BOB","dxvahd/DXVAHD_PROCESSOR_CAPS_DEINTERLACE_MOTION_COMPENSATION","dxvahd/DXVAHD_PROCESSOR_CAPS_FRAME_RATE_CONVERSION","dxvahd/DXVAHD_PROCESSOR_CAPS_INVERSE_TELECINE","mf.dxvahd_processor_caps"]
old-location: mf\dxvahd_processor_caps.htm
tech.root: mf
ms.assetid: 6fe6b1fe-4eef-427a-b28f-a359b066e552
ms.date: 12/05/2018
ms.keywords: DXVAHD_PROCESSOR_CAPS, DXVAHD_PROCESSOR_CAPS enumeration [Media Foundation], DXVAHD_PROCESSOR_CAPS_DEINTERLACE_ADAPTIVE, DXVAHD_PROCESSOR_CAPS_DEINTERLACE_BLEND, DXVAHD_PROCESSOR_CAPS_DEINTERLACE_BOB, DXVAHD_PROCESSOR_CAPS_DEINTERLACE_MOTION_COMPENSATION, DXVAHD_PROCESSOR_CAPS_FRAME_RATE_CONVERSION, DXVAHD_PROCESSOR_CAPS_INVERSE_TELECINE, dxvahd/DXVAHD_PROCESSOR_CAPS, dxvahd/DXVAHD_PROCESSOR_CAPS_DEINTERLACE_ADAPTIVE, dxvahd/DXVAHD_PROCESSOR_CAPS_DEINTERLACE_BLEND, dxvahd/DXVAHD_PROCESSOR_CAPS_DEINTERLACE_BOB, dxvahd/DXVAHD_PROCESSOR_CAPS_DEINTERLACE_MOTION_COMPENSATION, dxvahd/DXVAHD_PROCESSOR_CAPS_FRAME_RATE_CONVERSION, dxvahd/DXVAHD_PROCESSOR_CAPS_INVERSE_TELECINE, mf.dxvahd_processor_caps
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
req.typenames: DXVAHD_PROCESSOR_CAPS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVAHD_PROCESSOR_CAPS
 - dxvahd/_DXVAHD_PROCESSOR_CAPS
 - DXVAHD_PROCESSOR_CAPS
 - dxvahd/DXVAHD_PROCESSOR_CAPS
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
 - DXVAHD_PROCESSOR_CAPS
---

# DXVAHD_PROCESSOR_CAPS enumeration


## -description

Specifies the processing capabilities of a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.

## -enum-fields

### -field DXVAHD_PROCESSOR_CAPS_DEINTERLACE_BLEND:0x1

The video processor can perform blend deinterlacing.

 In <i>blend deinterlacing</i>, the two fields from an interlaced frame are blended into a single progressive frame. A video processor uses blend deinterlacing when it deinterlaces at half rate, as when converting 60i to 30p. Blend deinterlacing does not require reference frames.

### -field DXVAHD_PROCESSOR_CAPS_DEINTERLACE_BOB:0x2

The video processor can perform bob deinterlacing. 

In <i>bob deinterlacing</i>, missing field lines are interpolated from the lines above and below. Bob deinterlacing does not require reference frames.

### -field DXVAHD_PROCESSOR_CAPS_DEINTERLACE_ADAPTIVE:0x4

The video processor can perform adaptive deinterlacing.

<i>Adaptive deinterlacing</i> uses spatial or temporal interpolation, and switches between the two on a field-by-field basis, depending on the amount of motion. If the video processor does not receive enough reference frames to perform adaptive deinterlacing, it falls back to bob deinterlacing.

### -field DXVAHD_PROCESSOR_CAPS_DEINTERLACE_MOTION_COMPENSATION:0x8

The video processor  can perform motion-compensated deinterlacing.

<i>Motion-compensated deinterlacing</i> uses motion vectors to recreate missing lines. If the video processor does not receive enough reference frames to perform motion-compensated deinterlacing, it falls back to bob deinterlacing.

### -field DXVAHD_PROCESSOR_CAPS_INVERSE_TELECINE:0x10

The video processor can perform inverse telecine (IVTC).

 If the video processor supports this capability, the <b>ITelecineCaps</b> member of the <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps">DXVAHD_VPCAPS</a> structure specifies which IVTC modes are supported.

### -field DXVAHD_PROCESSOR_CAPS_FRAME_RATE_CONVERSION:0x20

The video processor can convert the frame rate by interpolating frames.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/medfound/direct3d-video-enumerations">Direct3D Video Enumerations</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
