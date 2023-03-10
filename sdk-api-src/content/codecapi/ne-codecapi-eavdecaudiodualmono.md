---
UID: NE:codecapi.eAVDecAudioDualMono
title: eAVDecAudioDualMono (codecapi.h)
description: Specifies whether the input audio stream is stereo or dual mono. This enumeration is used with the AVDecAudioDualMono property.
helpviewer_keywords: ["codecapi/eAVDecAudioDualMono","codecapi/eAVDecAudioDualMono_IsDualMono","codecapi/eAVDecAudioDualMono_IsNotDualMono","codecapi/eAVDecAudioDualMono_UnSpecified","dshow.eavdecaudiodualmono","eAVDecAudioDualMono","eAVDecAudioDualMono enumeration [DirectShow]","eAVDecAudioDualMonoEnumeration","eAVDecAudioDualMono_IsDualMono","eAVDecAudioDualMono_IsNotDualMono","eAVDecAudioDualMono_UnSpecified"]
old-location: dshow\eavdecaudiodualmono.htm
tech.root: dshow
ms.assetid: d9d3cc66-5622-4641-b302-6ecc6a05b1aa
ms.date: 12/05/2018
ms.keywords: codecapi/eAVDecAudioDualMono, codecapi/eAVDecAudioDualMono_IsDualMono, codecapi/eAVDecAudioDualMono_IsNotDualMono, codecapi/eAVDecAudioDualMono_UnSpecified, dshow.eavdecaudiodualmono, eAVDecAudioDualMono, eAVDecAudioDualMono enumeration [DirectShow], eAVDecAudioDualMonoEnumeration, eAVDecAudioDualMono_IsDualMono, eAVDecAudioDualMono_IsNotDualMono, eAVDecAudioDualMono_UnSpecified
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
 - eAVDecAudioDualMono
 - codecapi/eAVDecAudioDualMono
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
 - eAVDecAudioDualMono
---

# eAVDecAudioDualMono enumeration


## -description

Specifies whether the input audio stream is stereo or dual mono. This enumeration is used with the <a href="/windows/desktop/DirectShow/avdecaudiodualmono-property">AVDecAudioDualMono</a> property.

## -enum-fields

### -field eAVDecAudioDualMono_IsNotDualMono:0

The input bit stream is not dual mono.

### -field eAVDecAudioDualMono_IsDualMono:1

The input bit stream is dual mono.

### -field eAVDecAudioDualMono_UnSpecified:2  

There is no indication in the bit stream whether the audio is dual mono.

## -remarks

In dual mono encoding, each channel is encoded separately. In stereo encoding, both channels are encoded together.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
