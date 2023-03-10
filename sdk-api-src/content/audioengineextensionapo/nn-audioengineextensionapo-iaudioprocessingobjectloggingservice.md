---
UID: NN:audioengineextensionapo.IAudioProcessingObjectLoggingService
tech.root: audio
title: IAudioProcessingObjectLoggingService
ms.date: 06/19/2021
targetos: Windows
description: Represents a logging service for APOs.
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
 - IAudioProcessingObjectLoggingService
f1_keywords:
 - IAudioProcessingObjectLoggingService
 - audioengineextensionapo/IAudioProcessingObjectLoggingService
dev_langs:
 - c++
---

## -description

Represents a logging service for APOs.

## -remarks

Get an instance of this interface by [QueryService](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) on the object in the *pServiceProvider* field of the [APOInitSystemEffects3](nn-audioengineextensionapo-iaudiosystemeffects3.md) structure passed in the *pbyData* parameter to [IAudioProcessingObject::Initialize](/windows/win32/api/audioenginebaseapo/nf-audioenginebaseapo-iaudioprocessingobject-initialize). Specify **SID_AudioProcessingObjectLoggingService** as the identifier in the *guidService* parameter. 

> [!NOTE]
> [IAudioProcessingObjectLoggingService::ApoLog](nf-audioengineextensionapo-iaudioprocessingobjectloggingservice-apolog.md) should never be called from a real-time priority thread. For more information on thread priorities, see [Scheduling Priorities](/windows/win32/procthread/scheduling-priorities).

For more information on the Windows 11 APIs for the Audio Processing Objects (APOs) that can ship with audio drivers, see [Windows 11 APIs for Audio Processing Objects](/windows-hardware/drivers/audio/windows-11-apis-for-audio-processing-objects).

## -see-also

