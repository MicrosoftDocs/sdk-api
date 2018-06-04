---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# __MIDL___MIDL_itf_mmdeviceapi_0000_0000_0002 enumeration


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

The number of members in the <a href="https://msdn.microsoft.com/0d0d3174-8489-4951-858c-024d58477ae0">ERole</a> enumeration (not counting the ERole_enum_count member).


## -remarks



The <a href="https://msdn.microsoft.com/96776d2a-27b7-490a-b3a8-04782ec34f91">IMMDeviceEnumerator::GetDefaultAudioEndpoint</a> and <a href="https://msdn.microsoft.com/3d484e5d-bdc6-41f1-bd94-ab0c9e109222">IMMNotificationClient::OnDefaultDeviceChanged</a> methods use the constants defined in the <b>ERole</b> enumeration.

For more information, see <a href="https://msdn.microsoft.com/aa787004-0d3e-448b-80dd-92055f841aee">Device Roles</a>. 




## -see-also




<a href="https://msdn.microsoft.com/7d25be71-ffbe-4e8c-9a45-cdeb35d10292">Core Audio Enumerations</a>



<a href="https://msdn.microsoft.com/96776d2a-27b7-490a-b3a8-04782ec34f91">IMMDeviceEnumerator::GetDefaultAudioEndpoint</a>



<a href="https://msdn.microsoft.com/3d484e5d-bdc6-41f1-bd94-ab0c9e109222">IMMNotificationClient::OnDefaultDeviceChanged</a>
 

 

