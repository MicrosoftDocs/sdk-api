---
UID: NS:audioclientactivationparams.AUDIOCLIENT_PROCESS_LOOPBACK_PARAMS
tech.root: coreaudio
title: AUDIOCLIENT_PROCESS_LOOPBACK_PARAMS
ms.date: 01/21/2021
ms.topic: language-reference
targetos: Windows
description: Specifies parameters for a call to ActivateAudioInterfaceAsync where loopback activation is requested.
offlinehelp_keywords:
 - AUDIOCLIENT_PROCESS_LOOPBACK_PARAMS
 - audioclientactivationparams/AUDIOCLIENT_PROCESS_LOOPBACK_PARAMS
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
req.typenames: AUDIOCLIENT_PROCESS_LOOPBACK_PARAMS
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - audioclientactivationparams.h
api_name:
 - AUDIOCLIENT_PROCESS_LOOPBACK_PARAMS
f1_keywords:
 - AUDIOCLIENT_PROCESS_LOOPBACK_PARAMS
 - audioclientactivationparams/AUDIOCLIENT_PROCESS_LOOPBACK_PARAMS
dev_langs:
 - c++
---

## -description

Specifies parameters for a call to [ActivateAudioInterfaceAsync](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) where loopback activation is requested.

## -struct-fields

### -field TargetProcessId

The ID of the process for which the render streams, and the render streams of its child processes, will be included or excluded when activating the process loopback stream.

### -field ProcessLoopbackMode

A value from the [PROCESS_LOOPBACK_MODE](ne-audioclientactivationparams-process_loopback_mode.md) enumeration specifying whether the render streams for the process and child processes specified in the *TargetProcessId* field should be included or excluded when activating the audio interface. For sample code that demonstrates the process loopback capture scenario, see the [Application Loopback API Capture Sample](https://docs.microsoft.com/en-us/samples/microsoft/windows-classic-samples/applicationloopbackaudio-sample/).

## -remarks

## -see-also

