---
UID: NF:endpointvolume.IAudioEndpointVolumeCallback.OnNotify
title: IAudioEndpointVolumeCallback::OnNotify
author: windows-sdk-content
description: The OnNotify method notifies the client that the volume level or muting state of the audio endpoint device has changed.
old-location: coreaudio\iaudioendpointvolumecallback_onnotify.htm
old-project: CoreAudio
ms.assetid: a8ffad44-c621-4335-a312-16e7d6af2c18
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IAudioEndpointVolumeCallback interface [Core Audio],OnNotify method, IAudioEndpointVolumeCallback.OnNotify, IAudioEndpointVolumeCallback::OnNotify, IAudioEndpointVolumeCallbackOnNotify, OnNotify, OnNotify method [Core Audio], OnNotify method [Core Audio],IAudioEndpointVolumeCallback interface, coreaudio.iaudioendpointvolumecallback_onnotify, endpointvolume/IAudioEndpointVolumeCallback::OnNotify
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: endpointvolume.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: ProtType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Endpointvolume.h
api_name:
-	IAudioEndpointVolumeCallback.OnNotify
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IAudioEndpointVolumeCallback::OnNotify


## -description



The <b>OnNotify</b> method notifies the client that the volume level or muting state of the audio endpoint device has changed.




## -parameters




### -param pNotify [in]

Pointer to the volume-notification data. This parameter points to a structure of type <a href="https://msdn.microsoft.com/8778eb32-bc37-4d21-a096-f932db3d7b3f">AUDIO_VOLUME_NOTIFICATION_DATA</a>.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



The <i>pNotify</i> parameter points to a structure that describes the volume change event that initiated the call to <b>OnNotify</b>. This structure contains an event-context GUID. This GUID enables a client to distinguish between a volume (or muting) change that it initiated and one that some other client initiated. When calling an <a href="https://msdn.microsoft.com/5e3e7ffc-8822-4b1b-b9af-206ec1e767e2">IAudioEndpointVolume</a> method that changes the volume level of the stream, a client passes in a pointer to an event-context GUID that its implementation of the <b>OnNotify</b> method can recognize. The structure pointed to by <i>pNotify</i> contains this context GUID. If the client that changes the volume level supplies a <b>NULL</b> pointer value for the pointer to the event-context GUID, the value of the event-context GUID in the structure pointed to by <i>pNotify</i> is GUID_NULL.

The Windows 7, the system's volume user interface does not specify GUID_NULL when it changes the volume in the system.   A third-party OSD application can differentiate between master volume control changes that result from the system's volume user interface, and other volume changes such as changes from the built-in volume control handler.

For a code example that implements the <b>OnNotify</b> method, see <a href="https://msdn.microsoft.com/667c3659-69ae-469d-9ae0-e32a189cbc71">Endpoint Volume Controls</a>.




## -see-also




<a href="https://msdn.microsoft.com/8778eb32-bc37-4d21-a096-f932db3d7b3f">AUDIO_VOLUME_NOTIFICATION_DATA</a>



<a href="https://msdn.microsoft.com/5e3e7ffc-8822-4b1b-b9af-206ec1e767e2">IAudioEndpointVolume Interface</a>



<a href="https://msdn.microsoft.com/0b631d1b-f89c-4789-a09c-875b24a48a89">IAudioEndpointVolumeCallback Interface</a>
 

 

