---
UID: NS:mfapi._MT_CUSTOM_VIDEO_PRIMARIES
title: MT_CUSTOM_VIDEO_PRIMARIES (mfapi.h)
description: Defines custom color primaries for a video source. The color primaries define how to convert colors from RGB color space to CIE XYZ color space.
helpviewer_keywords: ["2c26e906-e428-4a76-b10a-10a18f300ebe","MT_CUSTOM_VIDEO_PRIMARIES","MT_CUSTOM_VIDEO_PRIMARIES structure [Media Foundation]","mf.mt_custom_video_primaries","mfapi/MT_CUSTOM_VIDEO_PRIMARIES"]
old-location: mf\mt_custom_video_primaries.htm
tech.root: mf
ms.assetid: 2c26e906-e428-4a76-b10a-10a18f300ebe
ms.date: 12/05/2018
ms.keywords: 2c26e906-e428-4a76-b10a-10a18f300ebe, MT_CUSTOM_VIDEO_PRIMARIES, MT_CUSTOM_VIDEO_PRIMARIES structure [Media Foundation], mf.mt_custom_video_primaries, mfapi/MT_CUSTOM_VIDEO_PRIMARIES
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: MT_CUSTOM_VIDEO_PRIMARIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MT_CUSTOM_VIDEO_PRIMARIES
 - mfapi/_MT_CUSTOM_VIDEO_PRIMARIES
 - MT_CUSTOM_VIDEO_PRIMARIES
 - mfapi/MT_CUSTOM_VIDEO_PRIMARIES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - MT_CUSTOM_VIDEO_PRIMARIES
---

# MT_CUSTOM_VIDEO_PRIMARIES structure


## -description

Defines custom color primaries for a video source. The color primaries define how to convert colors from RGB color space to CIE XYZ color space.

## -struct-fields

### -field fRx

Red x-coordinate.

### -field fRy

Red y-coordinate.

### -field fGx

Green x-coordinate.

### -field fGy

Green y-coordinate.

### -field fBx

Blue x-coordinate.

### -field fBy

Blue y-coordinate.

### -field fWx

White point x-coordinate.

### -field fWy

White point y-coordinate.

## -remarks

This structure is used with the <a href="/windows/desktop/medfound/mf-mt-custom-video-primaries-attribute">MF_MT_CUSTOM_VIDEO_PRIMARIES</a> attribute.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>