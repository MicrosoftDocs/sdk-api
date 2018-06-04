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
 

 

