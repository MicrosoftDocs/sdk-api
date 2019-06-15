---
UID: NE:mmdeviceapi.__MIDL___MIDL_itf_mmdeviceapi_0000_0000_0002
title: ERole (mmdeviceapi.h)
author: windows-sdk-content
description: The ERole enumeration defines constants that indicate the role that the system has assigned to an audio endpoint device.
old-location: coreaudio\erole.htm
tech.root: CoreAudio
ms.assetid: 0d0d3174-8489-4951-858c-024d58477ae0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ERole, ERole enumeration [Core Audio], ERole_enum_count, coreaudio.erole, eCommunications, eConsole, eMultimedia, mmdeviceapi/ERole, mmdeviceapi/ERole_enum_count, mmdeviceapi/eCommunications, mmdeviceapi/eConsole, mmdeviceapi/eMultimedia
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmdeviceapi.h
api_name:
 - ERole
product: Windows
targetos: Windows
req.typenames: ERole
req.redist: 
ms.custom: 19H1
---

# ERole enumeration


## -description



The <b>ERole</b> enumeration defines constants that indicate the role that the system has assigned to an audio endpoint device.




## -enum-fields




### -field eConsole

Games, system notification sounds, and voice commands.


### -field eMultimedia

Music, movies, narration, and live music recording.


### -field eCommunications

Voice communications (talking to another person).


### -field ERole_enum_count

The number of members in the <a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/ne-mmdeviceapi-__midl___midl_itf_mmdeviceapi_0000_0000_0002">ERole</a> enumeration (not counting the ERole_enum_count member).


## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint">IMMDeviceEnumerator::GetDefaultAudioEndpoint</a> and <a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondefaultdevicechanged">IMMNotificationClient::OnDefaultDeviceChanged</a> methods use the constants defined in the <b>ERole</b> enumeration.

For more information, see <a href="https://docs.microsoft.com/windows/desktop/CoreAudio/device-roles">Device Roles</a>. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-enumerations">Core Audio Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint">IMMDeviceEnumerator::GetDefaultAudioEndpoint</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondefaultdevicechanged">IMMNotificationClient::OnDefaultDeviceChanged</a>
 

 

