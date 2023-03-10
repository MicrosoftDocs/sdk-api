---
UID: NN:mmdeviceapi.IAudioSystemEffectsPropertyStore
tech.root: audio
title: IAudioSystemEffectsPropertyStore
ms.date: 06/18/2021
targetos: Windows
description: Provides access to manage audio system effects audio stores and to register for notifications when audio system effect properties change.
prerelease: false
req.assembly: 
req.construct-type: iface
req.ddi-compliance: 
req.header: mmdeviceapi.h
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
 - mmdeviceapi.h
api_name:
 - IAudioSystemEffectsPropertyStore
f1_keywords:
 - IAudioSystemEffectsPropertyStore
 - mmdeviceapi/IAudioSystemEffectsPropertyStore
dev_langs:
 - c++
---

## -description

Provides access to manage audio system effects audio stores and to register for notifications when audio system effect properties change.

## -remarks

This API is intended to support OEMs and app developers who want the ability to query and modify the property store associated with an audio device and publish HSA apps in the Microsoft Store. In order to use this API, you must specify the restricted *audioDeviceConfiguration* capability in your app package manifest. This is a restricted capability. For more information, see [App capability declarations](/windows/uwp/packaging/app-capability-declarations).

For more information on the Windows 11 APIs for the Audio Processing Objects (APOs) that can ship with audio drivers, see [Windows 11 APIs for Audio Processing Objects](/windows-hardware/drivers/audio/windows-11-apis-for-audio-processing-objects).

## -see-also


