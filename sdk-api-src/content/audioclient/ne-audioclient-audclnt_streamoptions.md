---
UID: NE:audioclient.AUDCLNT_STREAMOPTIONS
title: AUDCLNT_STREAMOPTIONS (audioclient.h)
description: Defines values that describe the characteristics of an audio stream.
helpviewer_keywords: ["AUDCLNT_STREAMOPTIONS","AUDCLNT_STREAMOPTIONS enumeration [Core Audio]","AUDCLNT_STREAMOPTIONS_MATCH_FORMAT","AUDCLNT_STREAMOPTIONS_NONE","AUDCLNT_STREAMOPTIONS_RAW","audioclient/AUDCLNT_STREAMOPTIONS","audioclient/AUDCLNT_STREAMOPTIONS_MATCH_FORMAT","audioclient/AUDCLNT_STREAMOPTIONS_NONE","audioclient/AUDCLNT_STREAMOPTIONS_RAW","coreaudio.audclnt_streamoptions"]
old-location: coreaudio\audclnt_streamoptions.htm
tech.root: CoreAudio
ms.assetid: C9A51FB2-46F5-4F20-B9F2-63EC53CAB3D7
ms.date: 12/05/2018
ms.keywords: AUDCLNT_STREAMOPTIONS, AUDCLNT_STREAMOPTIONS enumeration [Core Audio], AUDCLNT_STREAMOPTIONS_MATCH_FORMAT, AUDCLNT_STREAMOPTIONS_NONE, AUDCLNT_STREAMOPTIONS_RAW, audioclient/AUDCLNT_STREAMOPTIONS, audioclient/AUDCLNT_STREAMOPTIONS_MATCH_FORMAT, audioclient/AUDCLNT_STREAMOPTIONS_NONE, audioclient/AUDCLNT_STREAMOPTIONS_RAW, coreaudio.audclnt_streamoptions
req.header: audioclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
req.typenames: AUDCLNT_STREAMOPTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AUDCLNT_STREAMOPTIONS
 - audioclient/AUDCLNT_STREAMOPTIONS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - audioclient.h
api_name:
 - AUDCLNT_STREAMOPTIONS
---

# AUDCLNT_STREAMOPTIONS enumeration


## -description

Defines values  that describe the characteristics of an audio stream.

## -enum-fields

### -field AUDCLNT_STREAMOPTIONS_NONE

No stream options.

### -field AUDCLNT_STREAMOPTIONS_RAW

The audio stream is a 'raw' stream that bypasses
 all signal processing except for endpoint specific,
                                  always-on processing in the Audio Processing Object (APO), driver, and hardware.

### -field AUDCLNT_STREAMOPTIONS_MATCH_FORMAT

The audio client is requesting that the audio engine match the format proposed by the client. The audio engine
will match this format only if the format is supported by                                  the audio driver and associated APOs. 



Supported in Windows 10 and later.

### -field AUDCLNT_STREAMOPTIONS_AMBISONICS


### -field AUDCLNT_STREAMOPTIONS_POST_VOLUME_LOOPBACK

The audio client is requesting that the loopback stream tap into the playing audio after volume and/or mute settings have been applied. The default behavior is for the loopback stream to be tapped before volume and/or mute.

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-enumerations">Core Audio Enumerations</a>