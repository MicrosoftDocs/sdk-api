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

# IXAudio2EngineCallback::OnCriticalError


## -description


Called if a critical system error occurs that requires XAudio2 to be closed down and restarted.


## -parameters




### -param Error

Error code returned by XAudio2.


## -returns



This method does not return a value.




## -remarks



If you provide the ID of a  specific device in the <i>szDeviceId</i> parameter to   <a href="https://msdn.microsoft.com/2E8163C6-60E9-4EA9-AD5A-A7F3C84FF6CF">IXAudio2::CreateMasteringVoice</a> or use the XAUDIO2_NO_VIRTUAL_AUDIO_CLIENT flag, then a critical error will occur and <b>OnCriticalError</b> is raised if the underlying WASAPI rendering device becomes unavailable. This can occur when a headset or speaker is unplugged or when a USB audio device is removed, for example.   Once a critical error has occurred, audio processing stops and all further calls to XAudio2 fail. The only way to recover in this situation is to release the XAudio2 instance and create a new one.





If you specified NULL or  <i>szDeviceId</i> parameter to   <a href="https://msdn.microsoft.com/2E8163C6-60E9-4EA9-AD5A-A7F3C84FF6CF">IXAudio2::CreateMasteringVoice</a>, then the system uses a Virtual Audio Client to represent the audio endpoint. In this case, if the underlying WASAPI rendering device becomes unavailable, the system automatically selects a new audio rendering device for rendering, audio processing continues, and <b>OnCriticalError</b> is not raised.

On the mobile device family, a Virtual Audio Client is always used and <b>OnCriticalError</b> is never raised, regardless of the values you provide to    <a href="https://msdn.microsoft.com/2E8163C6-60E9-4EA9-AD5A-A7F3C84FF6CF">CreateMasteringVoice</a>.

For information about the <a href="https://msdn.microsoft.com/D71C117F-826F-41E9-98F4-C6024B3C5103">IXAudio2EngineCallback</a> interface methods, see the <a href="https://msdn.microsoft.com/4fbd4229-f7ac-33b3-b4b7-f09150a60598">XAudio2 Callbacks</a> section.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/D71C117F-826F-41E9-98F4-C6024B3C5103">IXAudio2EngineCallback</a>



<a href="https://msdn.microsoft.com/4fbd4229-f7ac-33b3-b4b7-f09150a60598">XAudio2 Callbacks</a>
 

 

