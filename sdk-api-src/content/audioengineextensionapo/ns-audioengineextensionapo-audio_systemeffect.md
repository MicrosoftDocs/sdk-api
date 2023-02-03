---
UID: NS:audioengineextensionapo.AUDIO_SYSTEMEFFECT
tech.root: Audio
title: AUDIO_SYSTEMEFFECT
ms.date: 06/17/2021
targetos: Windows
description: Represents a System Effects Audio Processing Object (sAPO) audio effect.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: audioengineextensionapo.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: 
req.target-type: 
req.typenames: AUDIO_SYSTEMEFFECT
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - audioengineextensionapo.h
api_name:
 - AUDIO_SYSTEMEFFECT
f1_keywords:
 - AUDIO_SYSTEMEFFECT
 - audioengineextensionapo/AUDIO_SYSTEMEFFECT
dev_langs:
 - c++
---

## -description

Represents a System Effects Audio Processing Object (sAPO) audio effect.

## -struct-fields

### -field id

The GUID identifier for an audio effect. Audio effect GUIDs are defined in [ksmedia.h](/windows-hardware/drivers/audio/ksmedia-h).

### -field canSetState

A boolean value specifying whether the effect state can be modified.

### -field state

A member of the [AUDIO_SYSTEMEFFECT_STATE](ne-audioengineextensionapo-audio_systemeffect_state.md) enumeration specifying the state of the audio effect.

## -remarks

For more information on the Windows 11 APIs for the Audio Processing Objects (APOs) that can ship with audio drivers, see [Windows 11 APIs for Audio Processing Objects](/windows-hardware/drivers/audio/windows-11-apis-for-audio-processing-objects).


## -see-also


