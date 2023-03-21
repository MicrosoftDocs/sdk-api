---
UID: NE:dxvahd._DXVAHD_ALPHA_FILL_MODE
title: DXVAHD_ALPHA_FILL_MODE (dxvahd.h)
description: Specifies how the output alpha values are calculated for Microsoft DirectX Video Acceleration High Definition (DXVA-HD) blit operations.
helpviewer_keywords: ["DXVAHD_ALPHA_FILL_MODE","DXVAHD_ALPHA_FILL_MODE enumeration [Media Foundation]","DXVAHD_ALPHA_FILL_MODE_BACKGROUND","DXVAHD_ALPHA_FILL_MODE_DESTINATION","DXVAHD_ALPHA_FILL_MODE_OPAQUE","DXVAHD_ALPHA_FILL_MODE_SOURCE_STREAM","dxvahd/DXVAHD_ALPHA_FILL_MODE","dxvahd/DXVAHD_ALPHA_FILL_MODE_BACKGROUND","dxvahd/DXVAHD_ALPHA_FILL_MODE_DESTINATION","dxvahd/DXVAHD_ALPHA_FILL_MODE_OPAQUE","dxvahd/DXVAHD_ALPHA_FILL_MODE_SOURCE_STREAM","mf.dxvahd_alpha_fill_mode"]
old-location: mf\dxvahd_alpha_fill_mode.htm
tech.root: mf
ms.assetid: f5e9f37e-5600-4139-86b2-7f63c2981b69
ms.date: 12/05/2018
ms.keywords: DXVAHD_ALPHA_FILL_MODE, DXVAHD_ALPHA_FILL_MODE enumeration [Media Foundation], DXVAHD_ALPHA_FILL_MODE_BACKGROUND, DXVAHD_ALPHA_FILL_MODE_DESTINATION, DXVAHD_ALPHA_FILL_MODE_OPAQUE, DXVAHD_ALPHA_FILL_MODE_SOURCE_STREAM, dxvahd/DXVAHD_ALPHA_FILL_MODE, dxvahd/DXVAHD_ALPHA_FILL_MODE_BACKGROUND, dxvahd/DXVAHD_ALPHA_FILL_MODE_DESTINATION, dxvahd/DXVAHD_ALPHA_FILL_MODE_OPAQUE, dxvahd/DXVAHD_ALPHA_FILL_MODE_SOURCE_STREAM, mf.dxvahd_alpha_fill_mode
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
req.typenames: DXVAHD_ALPHA_FILL_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVAHD_ALPHA_FILL_MODE
 - dxvahd/_DXVAHD_ALPHA_FILL_MODE
 - DXVAHD_ALPHA_FILL_MODE
 - dxvahd/DXVAHD_ALPHA_FILL_MODE
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
 - DXVAHD_ALPHA_FILL_MODE
---

# DXVAHD_ALPHA_FILL_MODE enumeration


## -description

Specifies how the output alpha values are calculated for Microsoft DirectX Video Acceleration High Definition (DXVA-HD) blit operations.

## -enum-fields

### -field DXVAHD_ALPHA_FILL_MODE_OPAQUE:0

Alpha values inside the target rectangle are set to opaque.

### -field DXVAHD_ALPHA_FILL_MODE_BACKGROUND:1

Alpha values inside the target rectangle are set to the alpha value specified in the background color. See <a href="/windows/win32/api/dxvahd/ns-dxvahd-dxvahd_blt_state_background_color_data">DXVAHD_BLT_STATE_BACKGROUND_COLOR</a>.

### -field DXVAHD_ALPHA_FILL_MODE_DESTINATION:2

Existing alpha values remain unchanged in the output surface.

### -field DXVAHD_ALPHA_FILL_MODE_SOURCE_STREAM:3

Alpha values from the input stream  are scaled and copied to the corresponding destination rectangle for that stream. If the input stream does not have alpha data, the DXVA-HD device sets the alpha values in the target rectangle to an opaque value. If the input stream is disabled or the source rectangle is empty, the alpha values in the target rectangle are not modified.

## -remarks

The <b>Mode</b> member of the <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_blt_state_alpha_fill_data">DXVAHD_BLT_STATE_ALPHA_FILL_DATA</a> structure has this enumeration type. That member specifies the alpha-fill mode for the input stream identified by the <b>StreamNumber</b> member of the same structure. To set the alpha-fill mode, call  <a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessbltstate">IDXVAHD_VideoProcessor::SetVideoProcessBltState</a>.

To find out which modes the device supports, call the <a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps">IDXVAHD_Device::GetVideoProcessorDeviceCaps</a> method. If the device sets the <b>DXVAHD_FEATURE_CAPS_ALPHA_FILL</b> flag in the <b>FeatureCaps</b> member of the <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps">DXVAHD_VPDEVCAPS</a> structure, the DXVA-HD device supports any of the modes listed here. Otherwise, the alpha-fill mode must be <b>DXVAHD_ALPHA_FILL_MODE_OPAQUE</b>.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_blt_state_alpha_fill_data">DXVAHD_BLT_STATE_ALPHA_FILL_DATA</a>



<a href="/windows/desktop/medfound/direct3d-video-enumerations">Direct3D Video Enumerations</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
