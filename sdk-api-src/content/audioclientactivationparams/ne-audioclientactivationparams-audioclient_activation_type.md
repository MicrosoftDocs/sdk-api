---
UID: NE:audioclientactivationparams.AUDIOCLIENT_ACTIVATION_TYPE
tech.root: coreaudio
title: AUDIOCLIENT_ACTIVATION_TYPE
ms.date: 01/21/2021
ms.topic: language-reference
targetos: Windows
description: Specifies the activation type for an AUDIOCLIENT_ACTIVATION_PARAMS structure passed into a call to ActivateAudioInterfaceAsync.
offlinehelp_keywords:
 - AUDIOCLIENT_ACTIVATION_TYPE
 - audioclientactivationparams/AUDIOCLIENT_ACTIVATION_TYPE
req.construct-type: enumeration
req.ddi-compliance: 
req.header: audioclientactivationparams.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - audioclientactivationparams.h
api_name:
 - AUDIOCLIENT_ACTIVATION_TYPE
f1_keywords:
 - AUDIOCLIENT_ACTIVATION_TYPE
 - audioclientactivationparams/AUDIOCLIENT_ACTIVATION_TYPE
dev_langs:
 - c++
---

## -description

Specifies the activation type for an [AUDIOCLIENT_ACTIVATION_PARAMS](ns-audioclientactivationparams-audioclient_activation_params.md) structure passed into a call to [ActivateAudioInterfaceAsync](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync).

## -enum-fields

### -field AUDIOCLIENT_ACTIVATION_TYPE_DEFAULT

Default activation.

### -field AUDIOCLIENT_ACTIVATION_TYPE_PROCESS_LOOPBACK

Process loopback activation, allowing for the inclusion or exclusion of audio rendered by the specified process and its child processes. For sample code that demonstrates the process loopback capture scenario, see the [Application Loopback API Capture Sample](https://docs.microsoft.com/en-us/samples/microsoft/windows-classic-samples/applicationloopbackaudio-sample/).

## -remarks

## -see-also

[AUDIOCLIENT_ACTIVATION_PARAMS](ns-audioclientactivationparams-audioclient_activation_params.md)

[ActivateAudioInterfaceAsync](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync)