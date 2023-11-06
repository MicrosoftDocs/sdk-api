---
UID: NE:codecapi.eAVEncDDAtoDConverterType
title: eAVEncDDAtoDConverterType (codecapi.h)
description: Specifies the type of analog-to-digital (A/D) conversion for a Dolby Digital audio stream. This enumeration is used with the AVEncDDAtoDConverterType property.
helpviewer_keywords: ["codecapi/eAVEncDDAtoDConverterType","codecapi/eAVEncDDAtoDConverterType_HDCD","codecapi/eAVEncDDAtoDConverterType_Standard","dshow.eavencddatodconvertertype","eAVEncDDAtoDConverterType","eAVEncDDAtoDConverterType enumeration [DirectShow]","eAVEncDDAtoDConverterType_HDCD","eAVEncDDAtoDConverterType_Standard"]
old-location: dshow\eavencddatodconvertertype.htm
tech.root: dshow
ms.assetid: 74f7a54a-dae8-46d0-bc99-c42fa548f4f1
ms.date: 4/26/2023
ms.keywords: codecapi/eAVEncDDAtoDConverterType, codecapi/eAVEncDDAtoDConverterType_HDCD, codecapi/eAVEncDDAtoDConverterType_Standard, dshow.eavencddatodconvertertype, eAVEncDDAtoDConverterType, eAVEncDDAtoDConverterType enumeration [DirectShow], eAVEncDDAtoDConverterType_HDCD, eAVEncDDAtoDConverterType_Standard
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
 - eAVEncDDAtoDConverterType
 - codecapi/eAVEncDDAtoDConverterType
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
 - eAVEncDDAtoDConverterType
---

# eAVEncDDAtoDConverterType enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Specifies the type of analog-to-digital (A/D) conversion for a Dolby Digital audio stream. This enumeration is used with the <a href="/windows/desktop/DirectShow/avencddatodconvertertype-property">AVEncDDAtoDConverterType</a> property.

## -enum-fields

### -field eAVEncDDAtoDConverterType_Standard:0

Standard.

### -field eAVEncDDAtoDConverterType_HDCD:1

High Definition Compatible Digital (HDCD).

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
