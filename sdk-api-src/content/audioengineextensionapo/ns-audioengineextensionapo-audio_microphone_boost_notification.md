---
UID: NS:audioengineextensionapo.AUDIO_MICROPHONE_BOOST_NOTIFICATION
tech.root: audio
title: AUDIO_MICROPHONE_BOOST_NOTIFICATION
ms.date: 02/28/2023
targetos: Windows
description: Represents an audio microphone boost APO notification.
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
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: AUDIO_MICROPHONE_BOOST_NOTIFICATION
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - audioengineextensionapo.h
api_name:
 - AUDIO_MICROPHONE_BOOST_NOTIFICATION
f1_keywords:
 - AUDIO_MICROPHONE_BOOST_NOTIFICATION
 - audioengineextensionapo/AUDIO_MICROPHONE_BOOST_NOTIFICATION
dev_langs:
 - c++
helpviewer_keywords:
 - AUDIO_MICROPHONE_BOOST_NOTIFICATION
---

## -description

Represents an audio microphone boost APO notification.

## -struct-fields

### -field endpoint

An [IMMDevice](..//mmdeviceapi/nn-mmdeviceapi-immdevice.md) representing the audio endpoint associated with the notification.

### -field eventContext

A GUID representing the context associated with the originator of the event. A client can use this method to keep track of control changes made by other processes and by the hardware. The functions [IAudioVolumeLevel::SetLevel](../devicetopology/nf-devicetopology-iperchanneldblevel-setlevel.md) and [IAudioMute::SetMute](../devicetopology/nf-devicetopology-iaudiomute-setmute) use the context. When this notification is recieved, a client can inspect the context GUID to discover whether it or another client is the source of the notification.

### -field microphoneBoostEnabled

A boolean value indicating the presence of a "Microphone Boost" part (connector or subunit) of an audio capture device topology.

### -field levelInDb

A float value specifying the volume level in decibels.

### -field levelMinInDb

A float value specifying the minimum volume level in decibels.

### -field levelMaxInDb

A float value specifying the maximum volume level in decibels.

### -field levelStepInDb

A float value specifying the stepping value between consecutive volume levels in the range *levelMinInDb* to *levelMaxInDb*.

### -field muteSupported

A boolean value indicating if the IAudioMute interface is supported by the "Microphone Boost" part of the audio capture device topology.

### -field mute

A boolean value indicating the current state (enabled or disabled) of the mute control

## -remarks

For more information on the Windows 11 APIs for the Audio Processing Objects (APOs) that can ship with audio drivers, see [Windows 11 APIs for Audio Processing Objects](/windows-hardware/drivers/audio/windows-11-apis-for-audio-processing-objects).


## -see-also

