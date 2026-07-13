---
UID: NF:audioengineextensionapo.IAudioSystemEffects3.SetAudioSystemEffectState
tech.root: Audio
title: IAudioSystemEffects3::SetAudioSystemEffectState
ms.date: 06/17/2021
targetos: Windows
description: Implemented by System Effects Audio Processing Object (sAPO) audio effects to allow the caller to set the state of effects.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: audioengineextensionapo.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - audioengineextensionapo.h
api_name:
 - IAudioSystemEffects3::SetAudioSystemEffectState
f1_keywords:
 - IAudioSystemEffects3::SetAudioSystemEffectState
 - audioengineextensionapo/IAudioSystemEffects3::SetAudioSystemEffectState
dev_langs:
 - c++
---

## -description

Implemented by System Effects Audio Processing Object (sAPO) audio effects to allow the caller to set the state of effects.

## -parameters

### -param effectId

The GUID identifier for an audio effect. Audio effect GUIDs are defined in [ksmedia.h](/windows-hardware/drivers/audio/ksmedia-h).


### -param state

A value from the [AUDIO_SYSTEMEFFECT_STATE](ne-audioengineextensionapo-audio_systemeffect_state.md) enumerating specifying the state to set.

## -returns

An HRESULT.

## -remarks

For more information on the Windows 11 APIs for the Audio Processing Objects (APOs) that can ship with audio drivers, see [Windows 11 APIs for Audio Processing Objects](/windows-hardware/drivers/audio/windows-11-apis-for-audio-processing-objects).

## -see-also

