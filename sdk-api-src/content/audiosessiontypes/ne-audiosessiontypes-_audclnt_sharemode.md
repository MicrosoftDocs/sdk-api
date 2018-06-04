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

# _AUDCLNT_SHAREMODE enumeration


## -description



The <b>AUDCLNT_SHAREMODE</b> enumeration defines constants that indicate whether an audio stream will run in shared mode or in exclusive mode.




## -enum-fields




### -field AUDCLNT_SHAREMODE_SHARED

The audio stream will run in shared mode. For more information, see Remarks.


### -field AUDCLNT_SHAREMODE_EXCLUSIVE

The audio stream will run in exclusive mode. For more information, see Remarks.


## -remarks



The <a href="https://msdn.microsoft.com/eb778503-06f8-4705-9f8d-9a4fd886ae27">IAudioClient::Initialize</a> and <a href="https://msdn.microsoft.com/92d1fc93-08e2-46d9-bd2f-ce1b2087d2d1">IAudioClient::IsFormatSupported</a> methods use the constants defined in the <b>AUDCLNT_SHAREMODE</b> enumeration.

In shared mode, the client can share the audio endpoint device with clients that run in other user-mode processes. The audio engine always supports formats for client streams that match the engine's mix format. In addition, the audio engine might support another format if the Windows audio service can insert system effects into the client stream to convert the client format to the mix format.

In exclusive mode, the Windows audio service attempts to establish a connection in which the client has exclusive access to the audio endpoint device. In this mode, the audio engine inserts no system effects into the local stream to aid in the creation of the connection point. Either the audio device can handle the specified format directly or the method fails.

For more information about shared-mode and exclusive-mode streams, see <a href="https://msdn.microsoft.com/b240b629-5bb6-4b07-95be-8ca5a14a3567">User-Mode Audio Components</a>.




## -see-also




<a href="https://msdn.microsoft.com/9dc9f182-3adf-4171-8829-35debae123da">Core Audio Constants</a>



<a href="https://msdn.microsoft.com/7d25be71-ffbe-4e8c-9a45-cdeb35d10292">Core Audio Enumerations</a>



<a href="https://msdn.microsoft.com/eb778503-06f8-4705-9f8d-9a4fd886ae27">IAudioClient::Initialize</a>



<a href="https://msdn.microsoft.com/92d1fc93-08e2-46d9-bd2f-ce1b2087d2d1">IAudioClient::IsFormatSupported</a>
 

 

