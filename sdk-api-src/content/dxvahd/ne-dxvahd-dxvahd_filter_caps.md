---
UID: NE:dxvahd._DXVAHD_FILTER_CAPS
title: DXVAHD_FILTER_CAPS (dxvahd.h)
description: Defines capabilities related to image adjustment and filtering for a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.
helpviewer_keywords: ["DXVAHD_FILTER_CAPS","DXVAHD_FILTER_CAPS enumeration [Media Foundation]","DXVAHD_FILTER_CAPS_ANAMORPHIC_SCALING","DXVAHD_FILTER_CAPS_BRIGHTNESS","DXVAHD_FILTER_CAPS_CONTRAST","DXVAHD_FILTER_CAPS_EDGE_ENHANCEMENT","DXVAHD_FILTER_CAPS_HUE","DXVAHD_FILTER_CAPS_NOISE_REDUCTION","DXVAHD_FILTER_CAPS_SATURATION","dxvahd/DXVAHD_FILTER_CAPS","dxvahd/DXVAHD_FILTER_CAPS_ANAMORPHIC_SCALING","dxvahd/DXVAHD_FILTER_CAPS_BRIGHTNESS","dxvahd/DXVAHD_FILTER_CAPS_CONTRAST","dxvahd/DXVAHD_FILTER_CAPS_EDGE_ENHANCEMENT","dxvahd/DXVAHD_FILTER_CAPS_HUE","dxvahd/DXVAHD_FILTER_CAPS_NOISE_REDUCTION","dxvahd/DXVAHD_FILTER_CAPS_SATURATION","mf.dxvahd_filter_caps"]
old-location: mf\dxvahd_filter_caps.htm
tech.root: mf
ms.assetid: 2f4e0b48-fbce-49e8-9ea8-1b6f0a022d60
ms.date: 12/05/2018
ms.keywords: DXVAHD_FILTER_CAPS, DXVAHD_FILTER_CAPS enumeration [Media Foundation], DXVAHD_FILTER_CAPS_ANAMORPHIC_SCALING, DXVAHD_FILTER_CAPS_BRIGHTNESS, DXVAHD_FILTER_CAPS_CONTRAST, DXVAHD_FILTER_CAPS_EDGE_ENHANCEMENT, DXVAHD_FILTER_CAPS_HUE, DXVAHD_FILTER_CAPS_NOISE_REDUCTION, DXVAHD_FILTER_CAPS_SATURATION, dxvahd/DXVAHD_FILTER_CAPS, dxvahd/DXVAHD_FILTER_CAPS_ANAMORPHIC_SCALING, dxvahd/DXVAHD_FILTER_CAPS_BRIGHTNESS, dxvahd/DXVAHD_FILTER_CAPS_CONTRAST, dxvahd/DXVAHD_FILTER_CAPS_EDGE_ENHANCEMENT, dxvahd/DXVAHD_FILTER_CAPS_HUE, dxvahd/DXVAHD_FILTER_CAPS_NOISE_REDUCTION, dxvahd/DXVAHD_FILTER_CAPS_SATURATION, mf.dxvahd_filter_caps
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
req.typenames: DXVAHD_FILTER_CAPS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVAHD_FILTER_CAPS
 - dxvahd/_DXVAHD_FILTER_CAPS
 - DXVAHD_FILTER_CAPS
 - dxvahd/DXVAHD_FILTER_CAPS
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
 - DXVAHD_FILTER_CAPS
---

# DXVAHD_FILTER_CAPS enumeration


## -description

Defines capabilities related to image adjustment and filtering for a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.

## -enum-fields

### -field DXVAHD_FILTER_CAPS_BRIGHTNESS:0x1

The device can adjust the brightness level.

### -field DXVAHD_FILTER_CAPS_CONTRAST:0x2

The device can adjust the contrast level.

### -field DXVAHD_FILTER_CAPS_HUE:0x4

The device can adjust hue.

### -field DXVAHD_FILTER_CAPS_SATURATION:0x8

The device can adjust the saturation level.

### -field DXVAHD_FILTER_CAPS_NOISE_REDUCTION:0x10

The device can perform noise reduction.

### -field DXVAHD_FILTER_CAPS_EDGE_ENHANCEMENT:0x20

The device can perform edge enhancement.

### -field DXVAHD_FILTER_CAPS_ANAMORPHIC_SCALING:0x40

The device can perform <i>anamorphic scaling</i>. Anamorphic scaling can be used to stretch 4:3 content to a widescreen 16:9 aspect ratio.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/medfound/direct3d-video-enumerations">Direct3D Video Enumerations</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
