---
UID: NE:mmdeviceapi.__MIDL___MIDL_itf_mmdeviceapi_0000_0000_0002
title: ERole (mmdeviceapi.h)
description: The ERole enumeration defines constants that indicate the role that the system has assigned to an audio endpoint device.
helpviewer_keywords: ["ERole","ERole enumeration [Core Audio]","ERole_enum_count","coreaudio.erole","eCommunications","eConsole","eMultimedia","mmdeviceapi/ERole","mmdeviceapi/ERole_enum_count","mmdeviceapi/eCommunications","mmdeviceapi/eConsole","mmdeviceapi/eMultimedia"]
old-location: coreaudio\erole.htm
tech.root: CoreAudio
ms.assetid: 0d0d3174-8489-4951-858c-024d58477ae0
ms.date: 12/05/2018
ms.keywords: ERole, ERole enumeration [Core Audio], ERole_enum_count, coreaudio.erole, eCommunications, eConsole, eMultimedia, mmdeviceapi/ERole, mmdeviceapi/ERole_enum_count, mmdeviceapi/eCommunications, mmdeviceapi/eConsole, mmdeviceapi/eMultimedia
req.header: mmdeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ERole
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_mmdeviceapi_0000_0000_0002
 - mmdeviceapi/__MIDL___MIDL_itf_mmdeviceapi_0000_0000_0002
 - ERole
 - mmdeviceapi/ERole
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmdeviceapi.h
api_name:
 - ERole
---

# ERole enumeration


## -description

The <b>ERole</b> enumeration defines constants that indicate the role that the system has assigned to an audio endpoint device.

## -enum-fields

### -field eConsole:0

Games, system notification sounds, and voice commands.

### -field eMultimedia

Music, movies, narration, and live music recording.

### -field eCommunications

Voice communications (talking to another person).

### -field ERole_enum_count

The number of members in the <a href="/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole">ERole</a> enumeration (not counting the ERole_enum_count member).

## -remarks

The <a href="/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole">IMMDeviceEnumerator::GetDefaultAudioEndpoint</a> and <a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondefaultdevicechanged">IMMNotificationClient::OnDefaultDeviceChanged</a> methods use the constants defined in the <b>ERole</b> enumeration.

For more information, see <a href="/windows/desktop/CoreAudio/device-roles">Device Roles</a>.

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-enumerations">Core Audio Enumerations</a>



<a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint">IMMDeviceEnumerator::GetDefaultAudioEndpoint</a>



<a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondefaultdevicechanged">IMMNotificationClient::OnDefaultDeviceChanged</a>
