---
UID: NN:audioengineextensionapo.IAudioProcessingObjectRTQueueService
tech.root: audio
title: IAudioProcessingObjectRTQueueService
ms.date: 06/19/2021
targetos: Windows
description: Represents a realtime work queue service for APOs.
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
 - IAudioProcessingObjectRTQueueService
f1_keywords:
 - IAudioProcessingObjectRTQueueService
 - audioengineextensionapo/IAudioProcessingObjectRTQueueService
dev_langs:
 - c++
---

## -description

Provides access to the real time work queue for APOs.

## -remarks

Get an instance of this interface by calling [QueryService](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) on the object in the *pServiceProvider* field of the [APOInitSystemEffects3](nn-audioengineextensionapo-iaudiosystemeffects3.md) structure passed in the *pbyData* parameter to [IAudioProcessingObject::Initialize](../audioenginebaseapo/nf-audioenginebaseapo-iaudioprocessingobject-initialize.md). Specify **SID_AudioProcessingObjectRTQueue** as the identifier in the *guidService* parameter.

For information on using the real-time work queue APIs, see [rtworkq.h header](../rtworkq/index.md).

For more information on the Windows 11 APIs for the Audio Processing Objects (APOs) that can ship with audio drivers, see [Windows 11 APIs for Audio Processing Objects](/windows-hardware/drivers/audio/windows-11-apis-for-audio-processing-objects).

## -see-also

