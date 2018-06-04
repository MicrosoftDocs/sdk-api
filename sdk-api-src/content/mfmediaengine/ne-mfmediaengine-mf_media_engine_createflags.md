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

# MF_MEDIA_ENGINE_CREATEFLAGS enumeration


## -description


Contains flags for the <a href="https://msdn.microsoft.com/EDEAD2C4-5695-4E63-9E9E-B09D75B60B7F">IMFMediaEngineClassFactory::CreateInstance</a>  method.


## -enum-fields




### -field MF_MEDIA_ENGINE_AUDIOONLY

The Media Engine will play audio only. It will not play video.


### -field MF_MEDIA_ENGINE_WAITFORSTABLE_STATE

The Media Engine's resource loading algorithm waits for the application to signal the thread that loads the resource. For more information, see the remarks for <b>MF_MEDIA_ENGINE_EVENT_NOTIFYSTABLESTATE</b> in the <a href="https://msdn.microsoft.com/05790FF8-0720-474B-AFF1-362E7A1B7C34">MF_MEDIA_ENGINE_EVENT</a> enumeration.


### -field MF_MEDIA_ENGINE_FORCEMUTE

Always mute the audio.


### -field MF_MEDIA_ENGINE_REAL_TIME_MODE

Enable low-latency mode in the rendering pipeline. This can be changed at a later time by calling <a href="https://msdn.microsoft.com/31534f69-33ec-41d3-93aa-f4c457649e48">IMFMediaEngineEx::SetRealTimeMode</a>.


### -field MF_MEDIA_ENGINE_DISABLE_LOCAL_PLUGINS

Disable locally registered media plugins. If this flag is set, the Media Engine will not load decoders or other media plugins that the application registered for the local process.


### -field MF_MEDIA_ENGINE_CREATEFLAGS_MASK

Reserved.


## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

