---
UID: NE:dxvahd._DXVAHD_FEATURE_CAPS
title: DXVAHD_FEATURE_CAPS (dxvahd.h)
description: Defines features that a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device can support.
helpviewer_keywords: ["DXVAHD_FEATURE_CAPS","DXVAHD_FEATURE_CAPS enumeration [Media Foundation]","DXVAHD_FEATURE_CAPS_ALPHA_FILL","DXVAHD_FEATURE_CAPS_ALPHA_PALETTE","DXVAHD_FEATURE_CAPS_CONSTRICTION","DXVAHD_FEATURE_CAPS_LUMA_KEY","dxvahd/DXVAHD_FEATURE_CAPS","dxvahd/DXVAHD_FEATURE_CAPS_ALPHA_FILL","dxvahd/DXVAHD_FEATURE_CAPS_ALPHA_PALETTE","dxvahd/DXVAHD_FEATURE_CAPS_CONSTRICTION","dxvahd/DXVAHD_FEATURE_CAPS_LUMA_KEY","mf.dxvahd_feature_caps"]
old-location: mf\dxvahd_feature_caps.htm
tech.root: mf
ms.assetid: 6014780b-3b8a-48d6-ae30-b48127a2c274
ms.date: 12/05/2018
ms.keywords: DXVAHD_FEATURE_CAPS, DXVAHD_FEATURE_CAPS enumeration [Media Foundation], DXVAHD_FEATURE_CAPS_ALPHA_FILL, DXVAHD_FEATURE_CAPS_ALPHA_PALETTE, DXVAHD_FEATURE_CAPS_CONSTRICTION, DXVAHD_FEATURE_CAPS_LUMA_KEY, dxvahd/DXVAHD_FEATURE_CAPS, dxvahd/DXVAHD_FEATURE_CAPS_ALPHA_FILL, dxvahd/DXVAHD_FEATURE_CAPS_ALPHA_PALETTE, dxvahd/DXVAHD_FEATURE_CAPS_CONSTRICTION, dxvahd/DXVAHD_FEATURE_CAPS_LUMA_KEY, mf.dxvahd_feature_caps
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
req.typenames: DXVAHD_FEATURE_CAPS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVAHD_FEATURE_CAPS
 - dxvahd/_DXVAHD_FEATURE_CAPS
 - DXVAHD_FEATURE_CAPS
 - dxvahd/DXVAHD_FEATURE_CAPS
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
 - DXVAHD_FEATURE_CAPS
---

# DXVAHD_FEATURE_CAPS enumeration


## -description

Defines features that a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device can support.

## -enum-fields

### -field DXVAHD_FEATURE_CAPS_ALPHA_FILL:0x1

The device can set the alpha values on the video output. See <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_blt_state_alpha_fill_data">DXVAHD_BLT_STATE_ALPHA_FILL_DATA</a>.

### -field DXVAHD_FEATURE_CAPS_CONSTRICTION:0x2

The device can downsample the video output. See <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_blt_state_constriction_data">DXVAHD_BLT_STATE_CONSTRICTION_DATA</a>.

### -field DXVAHD_FEATURE_CAPS_LUMA_KEY:0x4

The device can perform luma keying. See <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_stream_state_luma_key_data">DXVAHD_STREAM_STATE_LUMA_KEY_DATA</a>.

### -field DXVAHD_FEATURE_CAPS_ALPHA_PALETTE:0x8

The device can apply alpha values from color palette entries. See <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_stream_state_alpha_data">DXVAHD_STREAM_STATE_ALPHA_DATA</a>.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/medfound/direct3d-video-enumerations">Direct3D Video Enumerations</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
