---
UID: NE:mfmediaengine.MF_MEDIA_ENGINE_READY
title: MF_MEDIA_ENGINE_READY
author: windows-sdk-content
description: Defines ready-state values for the Media Engine.
old-location: mf\mf_media_engine_ready.htm
tech.root: medfound
ms.assetid: ADA5BBD6-B831-4C19-8770-318F0C5FDD6F
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: MF_MEDIA_ENGINE_READY, MF_MEDIA_ENGINE_READY enumeration [Media Foundation], MF_MEDIA_ENGINE_READY_HAVE_CURRENT_DATA, MF_MEDIA_ENGINE_READY_HAVE_ENOUGH_DATA, MF_MEDIA_ENGINE_READY_HAVE_FUTURE_DATA, MF_MEDIA_ENGINE_READY_HAVE_METADATA, MF_MEDIA_ENGINE_READY_HAVE_NOTHING, mf.mf_media_engine_ready, mfmediaengine/MF_MEDIA_ENGINE_READY, mfmediaengine/MF_MEDIA_ENGINE_READY_HAVE_CURRENT_DATA, mfmediaengine/MF_MEDIA_ENGINE_READY_HAVE_ENOUGH_DATA, mfmediaengine/MF_MEDIA_ENGINE_READY_HAVE_FUTURE_DATA, mfmediaengine/MF_MEDIA_ENGINE_READY_HAVE_METADATA, mfmediaengine/MF_MEDIA_ENGINE_READY_HAVE_NOTHING
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - mfmediaengine.h
api_name:
 - MF_MEDIA_ENGINE_READY
product: Windows
targetos: Windows
req.typenames: MF_MEDIA_ENGINE_READY
req.redist: 
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
 

 

