---
UID: NS:audioclientactivationparams.AUDIOCLIENT_ACTIVATION_PARAMS
tech.root: coreaudio
title: AUDIOCLIENT_ACTIVATION_PARAMS
ms.date: 01/21/2021
ms.topic: language-reference
targetos: Windows
description: Specifies the activation parameters for a call to ActivateAudioInterfaceAsync.
offlinehelp_keywords:
 - AUDIOCLIENT_ACTIVATION_PARAMS
 - audioclientactivationparams/AUDIOCLIENT_ACTIVATION_PARAMS
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: audioclientactivationparams.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: 
req.target-type: 
req.typenames: AUDIOCLIENT_ACTIVATION_PARAMS
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - audioclientactivationparams.h
api_name:
 - AUDIOCLIENT_ACTIVATION_PARAMS
f1_keywords:
 - AUDIOCLIENT_ACTIVATION_PARAMS
 - audioclientactivationparams/AUDIOCLIENT_ACTIVATION_PARAMS
dev_langs:
 - c++
---

## -description

Specifies the activation parameters for a call to [ActivateAudioInterfaceAsync](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync).

## -struct-fields

### -field ActivationType

A member of the [AUDIOCLIENT_ACTIVATION_TYPE](ne-audioclientactivationparams-audioclient_activation_type.md) specifying the type of audio interface activation. Currently default activation and loopback activation are supported.

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.ProcessLoopbackParams

A [AUDIOCLIENT_PROCESS_LOOPBACK_PARAMS](ns-audioclientactivationparams-audioclient_process_loopback_params.md) specifying the loopback parameters for the audio interface activation.

## -remarks

## -see-also

[AUDIOCLIENT_ACTIVATION_TYPE](ne-audioclientactivationparams-audioclient_activation_type.md)

[ActivateAudioInterfaceAsync](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync)
