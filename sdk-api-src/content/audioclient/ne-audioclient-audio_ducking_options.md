---
UID: NE:audioclient.AUDIO_DUCKING_OPTIONS
tech.root: CoreAudio
title: AUDIO_DUCKING_OPTIONS
ms.date: 02/08/2021
ms.topic: language-reference
targetos: Windows
description: Specifies audio ducking options. Use values from this enumeration when calling IAudioClientDuckingControl::SetDuckingOptionsForCurrentStream
req.construct-type: enumeration
req.ddi-compliance: 
req.header: audioclient.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - audioclient.h
api_name:
 - AUDIO_DUCKING_OPTIONS
f1_keywords:
 - AUDIO_DUCKING_OPTIONS
 - audioclient/AUDIO_DUCKING_OPTIONS
helpviewer_keywords:
 - AUDIO_DUCKING_OPTIONS
 - audioclient/AUDIO_DUCKING_OPTIONS
dev_langs:
 - c++
---

## -description

Specifies audio ducking options. Use values from this enumeration when calling [IAudioClientDuckingControl::SetDuckingOptionsForCurrentStream](nf-audioclient-iaudioclientduckingcontrol-setduckingoptionsforcurrentstream.md)

## -enum-fields

### -field AUDIO_DUCKING_OPTIONS_DEFAULT

The associated audio stream should use the default audio ducking behavior.

### -field AUDIO_DUCKING_OPTIONS_DO_NOT_DUCK_OTHER_STREAMS

The associated audio stream should not cause other streams to be ducked.

## -remarks

## -see-also

