---
UID: NN:audiostatemonitorapi.IAudioStateMonitor
tech.root: CoreAudio
title: IAudioStateMonitor
ms.date: 06/21/2023
targetos: Windows
description: Provides APIs for querying the sound level of audio streams and for receiving notifications when the sound level changes.
prerelease: false
req.assembly: 
req.construct-type: iface
req.ddi-compliance: 
req.header: audiostatemonitorapi.h
req.idl: 
req.include-header: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows build 19043
req.target-min-winversvr: 
req.target-type: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - audiostatemonitorapi.h
api_name:
 - IAudioStateMonitor
f1_keywords:
 - IAudioStateMonitor
 - audiostatemonitorapi/IAudioStateMonitor
dev_langs:
 - c++
helpviewer_keywords:
 - IAudioStateMonitor
---

## -description

Provides APIs for querying the sound level of audio streams and for receiving notifications when the sound level changes.

## -remarks

The method you use for instantiating the interface determines which audio streams are monitored. Factory methods are provided for monitoring capture and render streams, as well as monitoring streams based on audio category, device role, and audio device ID.

- [CreateCaptureAudioStateMonitor](nf-audiostatemonitorapi-createcaptureaudiostatemonitor.md)
- [CreateCaptureAudioStateMonitorForCategory](nf-audiostatemonitorapi-createcaptureaudiostatemonitorforcategory.md)
- [CreateCaptureAudioStateMonitorForCategoryAndDeviceId](nf-audiostatemonitorapi-createcaptureaudiostatemonitorforcategoryanddeviceid.md)
- [CreateCaptureAudioStateMonitorForCategoryAndDeviceRole](nf-audiostatemonitorapi-createcaptureaudiostatemonitorforcategoryanddevicerole.md)
- [CreateRenderAudioStateMonitor](nf-audiostatemonitorapi-createrenderaudiostatemonitor.md)
- [CreateRenderAudioStateMonitorForCategory](nf-audiostatemonitorapi-createrenderaudiostatemonitorforcategory.md)
- [CreateRenderAudioStateMonitorForCategoryAndDeviceId](nf-audiostatemonitorapi-createrenderaudiostatemonitorforcategoryanddeviceid.md)
- [CreateRenderAudioStateMonitorForCategoryAndDeviceRole](nf-audiostatemonitorapi-createrenderaudiostatemonitorforcategoryanddevicerole.md)

## -see-also

