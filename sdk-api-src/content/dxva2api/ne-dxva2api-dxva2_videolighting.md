---
UID: NE:dxva2api._DXVA2_VideoLighting
title: DXVA2_VideoLighting (dxva2api.h)
description: Describes the intended lighting conditions for viewing video content.
helpviewer_keywords: ["DXVA2_VideoLighting","DXVA2_VideoLighting enumeration [Media Foundation]","DXVA2_VideoLightingMask","DXVA2_VideoLighting_Unknown","DXVA2_VideoLighting_bright","DXVA2_VideoLighting_dark","DXVA2_VideoLighting_dim","DXVA2_VideoLighting_office","d70e7aa7-f68f-4ee3-bb75-dbe369e68f0e","dxva2api/DXVA2_VideoLighting","dxva2api/DXVA2_VideoLightingMask","dxva2api/DXVA2_VideoLighting_Unknown","dxva2api/DXVA2_VideoLighting_bright","dxva2api/DXVA2_VideoLighting_dark","dxva2api/DXVA2_VideoLighting_dim","dxva2api/DXVA2_VideoLighting_office","mf.dxva2_videolighting"]
old-location: mf\dxva2_videolighting.htm
tech.root: mf
ms.assetid: d70e7aa7-f68f-4ee3-bb75-dbe369e68f0e
ms.date: 12/05/2018
ms.keywords: DXVA2_VideoLighting, DXVA2_VideoLighting enumeration [Media Foundation], DXVA2_VideoLightingMask, DXVA2_VideoLighting_Unknown, DXVA2_VideoLighting_bright, DXVA2_VideoLighting_dark, DXVA2_VideoLighting_dim, DXVA2_VideoLighting_office, d70e7aa7-f68f-4ee3-bb75-dbe369e68f0e, dxva2api/DXVA2_VideoLighting, dxva2api/DXVA2_VideoLightingMask, dxva2api/DXVA2_VideoLighting_Unknown, dxva2api/DXVA2_VideoLighting_bright, dxva2api/DXVA2_VideoLighting_dark, dxva2api/DXVA2_VideoLighting_dim, dxva2api/DXVA2_VideoLighting_office, mf.dxva2_videolighting
req.header: dxva2api.h
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
req.typenames: DXVA2_VideoLighting
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVA2_VideoLighting
 - dxva2api/_DXVA2_VideoLighting
 - DXVA2_VideoLighting
 - dxva2api/DXVA2_VideoLighting
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxva2api.h
api_name:
 - DXVA2_VideoLighting
---

# DXVA2_VideoLighting enumeration


## -description

Describes the intended lighting conditions for viewing video content. These flags are used in the <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_extendedformat">DXVA2_ExtendedFormat</a> structure.

## -enum-fields

### -field DXVA2_VideoLightingMask:0xf

Bitmask to validate flag values. This value is not a valid flag.

### -field DXVA2_VideoLighting_Unknown:0

Unknown. Treat as DXVA2_VideoLighting_dim.

### -field DXVA2_VideoLighting_bright:1

Outdoor lighting.

### -field DXVA2_VideoLighting_office:2

Medium brightness; for example, an office.

### -field DXVA2_VideoLighting_dim:3

Dim; for example, a living room with a television and some additional low lighting.

### -field DXVA2_VideoLighting_dark:4

Dark; for example, a movie theater.

## -remarks

This enumeration is equivalent to the <b>DXVA_VideoLighting</b> enumeration used in DXVA 1.0.

If you are using the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface to describe the video format, the video lighting is specified in the <a href="/windows/desktop/medfound/mf-mt-video-lighting-attribute">MF_MT_VIDEO_LIGHTING</a> attribute.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
