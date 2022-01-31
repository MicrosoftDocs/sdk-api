---
UID: NE:codecapi.eAVEncInputVideoSystem
title: eAVEncInputVideoSystem (codecapi.h)
description: Specifies the nominal range for a video source. This enumeration is used with the AVEncInputVideoSystem property.
helpviewer_keywords: ["codecapi/eAVEncInputVideoSystem","codecapi/eAVEncInputVideoSystem_Component","codecapi/eAVEncInputVideoSystem_HDV","codecapi/eAVEncInputVideoSystem_MAC","codecapi/eAVEncInputVideoSystem_NTSC","codecapi/eAVEncInputVideoSystem_PAL","codecapi/eAVEncInputVideoSystem_SECAM","codecapi/eAVEncInputVideoSystem_Unspecified","dshow.eavencinputvideosystem","eAVEncInputVideoSystem","eAVEncInputVideoSystem enumeration [DirectShow]","eAVEncInputVideoSystemEnumeration","eAVEncInputVideoSystem_Component","eAVEncInputVideoSystem_HDV","eAVEncInputVideoSystem_MAC","eAVEncInputVideoSystem_NTSC","eAVEncInputVideoSystem_PAL","eAVEncInputVideoSystem_SECAM","eAVEncInputVideoSystem_Unspecified"]
old-location: dshow\eavencinputvideosystem.htm
tech.root: dshow
ms.assetid: f72be523-917a-439f-adc5-d7550e8d6cf9
ms.date: 12/05/2018
ms.keywords: codecapi/eAVEncInputVideoSystem, codecapi/eAVEncInputVideoSystem_Component, codecapi/eAVEncInputVideoSystem_HDV, codecapi/eAVEncInputVideoSystem_MAC, codecapi/eAVEncInputVideoSystem_NTSC, codecapi/eAVEncInputVideoSystem_PAL, codecapi/eAVEncInputVideoSystem_SECAM, codecapi/eAVEncInputVideoSystem_Unspecified, dshow.eavencinputvideosystem, eAVEncInputVideoSystem, eAVEncInputVideoSystem enumeration [DirectShow], eAVEncInputVideoSystemEnumeration, eAVEncInputVideoSystem_Component, eAVEncInputVideoSystem_HDV, eAVEncInputVideoSystem_MAC, eAVEncInputVideoSystem_NTSC, eAVEncInputVideoSystem_PAL, eAVEncInputVideoSystem_SECAM, eAVEncInputVideoSystem_Unspecified
req.header: codecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - eAVEncInputVideoSystem
 - codecapi/eAVEncInputVideoSystem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - codecapi.h
api_name:
 - eAVEncInputVideoSystem
---

# eAVEncInputVideoSystem enumeration


## -description

Specifies the nominal range for a video source. This enumeration is used with the <a href="/windows/desktop/DirectShow/avencinputvideosystem-property">AVEncInputVideoSystem</a> property.

## -enum-fields

### -field eAVEncInputVideoSystem_Unspecified:0

The video system is not specified.

### -field eAVEncInputVideoSystem_PAL:1

PAL television.

### -field eAVEncInputVideoSystem_NTSC:2

NTSC television.

### -field eAVEncInputVideoSystem_SECAM:3

SECAM television.

### -field eAVEncInputVideoSystem_MAC:4

Not documented for this release.

### -field eAVEncInputVideoSystem_HDV:5

High-definition (HD) video.

### -field eAVEncInputVideoSystem_Component:6

Component video.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
