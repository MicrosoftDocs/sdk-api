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

# MF_MEDIA_ENGINE_READY enumeration


## -description


Defines ready-state values for the Media Engine.


## -enum-fields




### -field MF_MEDIA_ENGINE_READY_HAVE_NOTHING

No data is available.


### -field MF_MEDIA_ENGINE_READY_HAVE_METADATA

Some metadata is available, including the duration and, for video files, the video dimensions. No media data is available.


### -field MF_MEDIA_ENGINE_READY_HAVE_CURRENT_DATA

There is media data  for the current playback position, but not enough data for playback or seeking.


### -field MF_MEDIA_ENGINE_READY_HAVE_FUTURE_DATA

There is enough media data to enable some playback or seeking. The amount of data might be a little as the next video frame.


### -field MF_MEDIA_ENGINE_READY_HAVE_ENOUGH_DATA

There is enough data to play the resource, based on the current rate at which the resource is being fetched. 


## -remarks



These values correspond to constants defined for the  <b>HTMLMediaElement.readyState</b> attribute  in HTML5.




## -see-also




<a href="https://msdn.microsoft.com/B8C9B600-87FD-4DE6-8794-5C1E41449554">IMFMediaEngine::GetReadyState</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

