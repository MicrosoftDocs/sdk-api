---
UID: NN:audioengineextensionapo.IAudioSystemEffects3
tech.root: audio
title: IAudioSystemEffects3
ms.date: 06/19/2021
targetos: Windows
description: Implemented by clients that require an APOInitSystemEffects3 structure to be passed into the IAudioProcessingObject::Initialize method.
prerelease: false
req.assembly: 
req.construct-type: iface
req.ddi-compliance: 
req.header: audioengineextensionapo.h
req.idl: 
req.include-header: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: 
req.target-type: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - audioengineextensionapo.h
api_name:
 - IAudioSystemEffects3
f1_keywords:
 - IAudioSystemEffects3
 - audioengineextensionapo/IAudioSystemEffects3
dev_langs:
 - c++
---

## -description

Implementing this interface also implies that the APO supports the APO Settings framework and allows the APO to subscribe for common audio related notifications from the Audio Engine

This interface is also implemented by clients that require an [APOInitSystemEffects3](ns-audioengineextensionapo-apoinitsystemeffects3.md) structure to be passed into the [IAudioProcessingObject::Initialize](..//audioenginebaseapo/nf-audioenginebaseapo-iaudioprocessingobject-initialize.md) method. **APOInitSystemEffects3** adds the ability to obtain a service provider such as [IAudioProcessingObjectLoggingService](nn-audioengineextensionapo-iaudioprocessingobjectloggingservice.md) or [IAudioProcessingObjectRTQueueService](nn-audioengineextensionapo-iaudioprocessingobjectrtqueueservice.md). 

> [!NOTE]
> On OS versions earlier than Windows Build 22000, the system will not pass an **APOInitSystemEffects3** into **IAudioProcessingObject::Initialize** even if the client implements **IAudioSystemEffects3**, but will instead pass an older version of the structure, [APOInitSystemEffects2](/windows/win32/api/audioenginebaseapo/ns-audioenginebaseapo-apoinitsystemeffects2) or [APOInitSystemEffects](/windows/win32/api/audioenginebaseapo/ns-audioenginebaseapo-apoinitsystemeffects), into **Initialize**.

## -remarks

For more information on the Windows 11 APIs for the Audio Processing Objects (APOs) that can ship with audio drivers, see [Windows 11 APIs for Audio Processing Objects](/windows-hardware/drivers/audio/windows-11-apis-for-audio-processing-objects).

## -see-also

