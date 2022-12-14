---
UID: NE:audioclientactivationparams.PROCESS_LOOPBACK_MODE
tech.root: coreaudio
title: PROCESS_LOOPBACK_MODE
ms.date: 01/21/2021
ms.topic: language-reference
targetos: Windows
description: Specifies the loopback mode for an AUDIOCLIENT_ACTIVATION_PARAMS structure passed into a call to ActivateAudioInterfaceAsync.
offlinehelp_keywords:
 - PROCESS_LOOPBACK_MODE
 - audioclientactivationparams/PROCESS_LOOPBACK_MODE
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
 - PROCESS_LOOPBACK_MODE
f1_keywords:
 - PROCESS_LOOPBACK_MODE
 - audioclientactivationparams/PROCESS_LOOPBACK_MODE
dev_langs:
 - c++
---

## -description

Specifies the loopback mode for an [AUDIOCLIENT_ACTIVATION_PARAMS](ns-audioclientactivationparams-audioclient_activation_params.md) structure passed into a call to [ActivateAudioInterfaceAsync](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync).

## -enum-fields

### -field PROCESS_LOOPBACK_MODE_INCLUDE_TARGET_PROCESS_TREE

Render streams from the specified process and its child processes are included in the activated process loopback stream.

### -field PROCESS_LOOPBACK_MODE_EXCLUDE_TARGET_PROCESS_TREE

Render streams from the specified process and its child processes are excluded from the activated process loopback stream.

## -remarks

## -see-also

[AUDIOCLIENT_ACTIVATION_PARAMS](ns-audioclientactivationparams-audioclient_activation_params.md)
[ActivateAudioInterfaceAsync](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync)
