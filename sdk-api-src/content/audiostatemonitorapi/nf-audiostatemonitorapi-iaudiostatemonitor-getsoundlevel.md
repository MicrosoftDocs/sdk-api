---
UID: NF:audiostatemonitorapi.IAudioStateMonitor.GetSoundLevel
tech.root: CoreAudio
title: IAudioStateMonitor::GetSoundLevel
ms.date: 06/21/2023
targetos: Windows
description: Gets the current sound level for the audio streams associated with an IAudioStateMonitor.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: audiostatemonitorapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows build 19043
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
 - audiostatemonitorapi.h
api_name:
 - IAudioStateMonitor::GetSoundLevel
f1_keywords:
 - IAudioStateMonitor::GetSoundLevel
 - audiostatemonitorapi/IAudioStateMonitor::GetSoundLevel
dev_langs:
 - c++
helpviewer_keywords:
 - GetSoundLevel
---

## -description

Gets the current sound level for the audio streams associated with an [IAudioStateMonitor](nn-audiostatemonitorapi-iaudiostatemonitor.md).

## -returns

A value from the [AudioStateMonitorSoundLevel](ne-audiostatemonitorapi-audiostatemonitorsoundlevel.md) enumeration specifying the current sound level for the audio stream.

## -remarks

Windows dynamically mutes or lowers the level of audio streams in response to system events. For example, the volume of a podcast app's audio render stream may be lowered while an alarm is ringing. Or an audio recording app may have their capture stream muted when the app moves to the background. Register an implementation of the [AudioStateMonitorCallback](nc-audiostatemonitorapi-audiostatemonitorcallback.md) event to receive notifications when the sound level for a category of audio streams changes.

## -see-also

