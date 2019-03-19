---
UID: NE:mmdeviceapi.__MIDL___MIDL_itf_mmdeviceapi_0000_0000_0002
title: ERole (mmdeviceapi.h)
author: windows-sdk-content
description: The ERole enumeration defines constants that indicate the role that the system has assigned to an audio endpoint device.
old-location: coreaudio\erole.htm
tech.root: CoreAudio
ms.assetid: 0d0d3174-8489-4951-858c-024d58477ae0
ms.author: windowssdkdev
ms.date: 12/5/2018
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

The number of members in the <a href="https://msdn.microsoft.com/en-us/library/Dd370842(v=VS.85).aspx">ERole</a> enumeration (not counting the ERole_enum_count member).


## -remarks



The <a href="https://msdn.microsoft.com/96776d2a-27b7-490a-b3a8-04782ec34f91">IMMDeviceEnumerator::GetDefaultAudioEndpoint</a> and <a href="https://msdn.microsoft.com/3d484e5d-bdc6-41f1-bd94-ab0c9e109222">IMMNotificationClient::OnDefaultDeviceChanged</a> methods use the constants defined in the <b>ERole</b> enumeration.

For more information, see <a href="https://msdn.microsoft.com/aa787004-0d3e-448b-80dd-92055f841aee">Device Roles</a>. 




## -see-also




<a href="https://msdn.microsoft.com/7d25be71-ffbe-4e8c-9a45-cdeb35d10292">Core Audio Enumerations</a>



<a href="https://msdn.microsoft.com/96776d2a-27b7-490a-b3a8-04782ec34f91">IMMDeviceEnumerator::GetDefaultAudioEndpoint</a>



<a href="https://msdn.microsoft.com/3d484e5d-bdc6-41f1-bd94-ab0c9e109222">IMMNotificationClient::OnDefaultDeviceChanged</a>
 

 

