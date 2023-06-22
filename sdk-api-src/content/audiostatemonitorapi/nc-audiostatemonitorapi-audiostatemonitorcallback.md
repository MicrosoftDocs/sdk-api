---
UID: NC:audiostatemonitorapi.AudioStateMonitorCallback
tech.root: CoreAudio
title: AudioStateMonitorCallback
ms.date: 06/21/2023
targetos: Windows
description: Occurs when the system changes the sound level of the audio streams being monitored by an IAudioStreamStateMonitor.
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
 - LibDef
api_location:
 - audiostatemonitorapi.h
api_name:
 - AudioStateMonitorCallback
f1_keywords:
 - AudioStateMonitorCallback
 - audiostatemonitorapi/AudioStateMonitorCallback
dev_langs:
 - c++
helpviewer_keywords:
 - AudioStateMonitorCallback
---

## -description

Called when the system changes the sound level of the audio streams being monitored by an [IAudioStateMonitor](nn-audiostatemonitorapi-iaudiostatemonitor.md).

## -parameters

### -param audioStateMonitor [in]

The **IAudioStateMonitor** with which the callback was registered.

### -param context [in, optional]

A void pointer that points to context information provided by the client in the call to [IAudioStateMonitor::RegisterCallback](nf-audiostatemonitorapi-iaudiostatemonitor-registercallback.md).

## -remarks

Windows dynamically mutes or lowers the level of audio streams in response to system events. For example, the volume of a podcast app's audio render stream may be lowered while an alarm is ringing. Or an audio recording app may have their capture stream muted when the app moves to the background. Register an implementation of this callback with a call to [IAudioStateMonitor::RegisterCallback](nf-audiostatemonitorapi-iaudiostatemonitor-registercallback.md) to receive notifications when the sound level for a stream changes, and then call [IAudioStateMonitor::GetSoundLevel](nf-audiostatemonitorapi-iaudiostatemonitor-getsoundlevel.md) property to determine the new current audio level.



## -see-also

