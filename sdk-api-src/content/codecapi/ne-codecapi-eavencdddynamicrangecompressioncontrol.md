---
UID: NE:codecapi.eAVEncDDDynamicRangeCompressionControl
title: eAVEncDDDynamicRangeCompressionControl (codecapi.h)
description: Specifies the dynamic range control profile in a Dolby Digital audio stream. This enumeration is used with the AVEncDDDynamicRangeCompressionControl property.
helpviewer_keywords: ["codecapi/eAVEncDDDynamicRangeCompressionControl","codecapi/eAVEncDDDynamicRangeCompressionControl_FilmLight","codecapi/eAVEncDDDynamicRangeCompressionControl_FilmStandard","codecapi/eAVEncDDDynamicRangeCompressionControl_MusicLight","codecapi/eAVEncDDDynamicRangeCompressionControl_MusicStandard","codecapi/eAVEncDDDynamicRangeCompressionControl_None","codecapi/eAVEncDDDynamicRangeCompressionControl_Speech","dshow.eavencdddynamicrangecompressioncontrol","eAVEncDDDynamicRangeCompressionControl","eAVEncDDDynamicRangeCompressionControl enumeration [DirectShow]","eAVEncDDDynamicRangeCompressionControlEnumeration","eAVEncDDDynamicRangeCompressionControl_FilmLight","eAVEncDDDynamicRangeCompressionControl_FilmStandard","eAVEncDDDynamicRangeCompressionControl_MusicLight","eAVEncDDDynamicRangeCompressionControl_MusicStandard","eAVEncDDDynamicRangeCompressionControl_None","eAVEncDDDynamicRangeCompressionControl_Speech"]
old-location: dshow\eavencdddynamicrangecompressioncontrol.htm
tech.root: dshow
ms.assetid: bbe81ff1-a30d-4eee-a2ca-8a1c464492fa
ms.date: 12/05/2018
ms.keywords: codecapi/eAVEncDDDynamicRangeCompressionControl, codecapi/eAVEncDDDynamicRangeCompressionControl_FilmLight, codecapi/eAVEncDDDynamicRangeCompressionControl_FilmStandard, codecapi/eAVEncDDDynamicRangeCompressionControl_MusicLight, codecapi/eAVEncDDDynamicRangeCompressionControl_MusicStandard, codecapi/eAVEncDDDynamicRangeCompressionControl_None, codecapi/eAVEncDDDynamicRangeCompressionControl_Speech, dshow.eavencdddynamicrangecompressioncontrol, eAVEncDDDynamicRangeCompressionControl, eAVEncDDDynamicRangeCompressionControl enumeration [DirectShow], eAVEncDDDynamicRangeCompressionControlEnumeration, eAVEncDDDynamicRangeCompressionControl_FilmLight, eAVEncDDDynamicRangeCompressionControl_FilmStandard, eAVEncDDDynamicRangeCompressionControl_MusicLight, eAVEncDDDynamicRangeCompressionControl_MusicStandard, eAVEncDDDynamicRangeCompressionControl_None, eAVEncDDDynamicRangeCompressionControl_Speech
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
 - eAVEncDDDynamicRangeCompressionControl
 - codecapi/eAVEncDDDynamicRangeCompressionControl
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
 - eAVEncDDDynamicRangeCompressionControl
---

# eAVEncDDDynamicRangeCompressionControl enumeration


## -description

Specifies the dynamic range control profile in a Dolby Digital audio stream. This enumeration is used with the <a href="/windows/desktop/DirectShow/avencdddynamicrangecompressioncontrol-property">AVEncDDDynamicRangeCompressionControl</a> property.

## -enum-fields

### -field eAVEncDDDynamicRangeCompressionControl_None:0

No dynamic range compression.

### -field eAVEncDDDynamicRangeCompressionControl_FilmStandard:1

Film standard profile.

### -field eAVEncDDDynamicRangeCompressionControl_FilmLight:2

Film light profile.

### -field eAVEncDDDynamicRangeCompressionControl_MusicStandard:3

Music standard profile.

### -field eAVEncDDDynamicRangeCompressionControl_MusicLight:4

Music light profile.

### -field eAVEncDDDynamicRangeCompressionControl_Speech:5

Speech profile.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
