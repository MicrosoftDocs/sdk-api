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

# IAudioDeviceEndpoint::GetEventDrivenCapable


## -description



        The <b>GetEventDrivenCapable</b> method indicates whether the device endpoint is event driven. The device endpoint controls the period of the audio engine  by setting events that signal buffer availability.


## -parameters




### -param pbisEventCapable






#### - pbIsEventCapable [out]

A value of <b>TRUE</b> indicates that the device endpoint is event driven. A value of <b>FALSE</b> indicates that it is not event driven. If the endpoint device is event driven, the audio engine can receive events from an audio device endpoint.


## -returns



If the method succeeds, it returns <b>S_OK</b>.




## -remarks



Call the <b>GetEventDrivenCapable</b> method before     calling the <a href="https://msdn.microsoft.com/345a172b-11af-4c98-9f9c-54bfa38c5077">IAudioDeviceEndpoint::SetBuffer</a>method, which initializes the device endpoint and creates a buffer. This allows the device endpoint to set up the structures needed for driving events.

If the audio engine requires an event driven device endpoint, it will:

<ul>
<li>Create an event and set the event handle on the device endpoint by calling the <a href="https://msdn.microsoft.com/9f0f216a-d785-42e9-b07d-f1f2568b5833">IAudioEndpoint::SetEventHandle</a> method.</li>
<li>Specify event driven mode by setting the <b>AUDCLNT_STREAMFLAGS_EVENTCALLBACK</b> flag on the device endpoint by calling the <a href="https://msdn.microsoft.com/f6713912-ba7e-4e3e-95d9-8318c40a7042">IAudioEndpoint::SetStreamFlags</a> method.</li>
</ul>
The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.




## -see-also




<a href="https://msdn.microsoft.com/3112bc7e-e138-4b42-8f82-61fdf19f7e94">IAudioDeviceEndpoint</a>
 

 

