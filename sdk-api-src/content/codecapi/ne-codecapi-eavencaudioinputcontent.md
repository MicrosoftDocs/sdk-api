---
UID: NE:codecapi.eAVEncAudioInputContent
title: eAVEncAudioInputContent (codecapi.h)
description: Specifies whether the audio content contains music or voice. This enumeration is used with the AVEncAudioInputContent property.
helpviewer_keywords: ["AVEncAudioInputContent_Music","AVEncAudioInputContent_Unknown","AVEncAudioInputContent_Voice","codecapi/AVEncAudioInputContent_Music","codecapi/AVEncAudioInputContent_Unknown","codecapi/AVEncAudioInputContent_Voice","codecapi/eAVEncAudioInputContent","dshow.eavencaudioinputcontent","eAVEncAudioInputContent","eAVEncAudioInputContent enumeration [DirectShow]","eAVEncAudioInputContentEnumeration"]
old-location: dshow\eavencaudioinputcontent.htm
tech.root: dshow
ms.assetid: e9de2468-3676-4b4b-8eec-385c33b3f44b
ms.date: 12/05/2018
ms.keywords: AVEncAudioInputContent_Music, AVEncAudioInputContent_Unknown, AVEncAudioInputContent_Voice, codecapi/AVEncAudioInputContent_Music, codecapi/AVEncAudioInputContent_Unknown, codecapi/AVEncAudioInputContent_Voice, codecapi/eAVEncAudioInputContent, dshow.eavencaudioinputcontent, eAVEncAudioInputContent, eAVEncAudioInputContent enumeration [DirectShow], eAVEncAudioInputContentEnumeration
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
 - eAVEncAudioInputContent
 - codecapi/eAVEncAudioInputContent
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
 - eAVEncAudioInputContent
---

# eAVEncAudioInputContent enumeration


## -description

Specifies whether the audio content contains music or voice. This enumeration is used with the <a href="/windows/desktop/DirectShow/avencaudioinputcontent-property">AVEncAudioInputContent</a> property.

## -enum-fields

### -field AVEncAudioInputContent_Unknown:0

The audio content is not known.

### -field AVEncAudioInputContent_Voice:1

The audio contains voice.

### -field AVEncAudioInputContent_Music:2

The audio contains music.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
