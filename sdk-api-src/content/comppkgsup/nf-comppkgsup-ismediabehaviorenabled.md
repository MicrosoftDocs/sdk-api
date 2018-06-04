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

# IsMediaBehaviorEnabled function


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Gets a value indicating whether the media behavior associated with the specified GUID is enabled.


## -parameters




### -param mediaBehavior

A GUID that specifies the media behavior for which the enabled state is queried.


## -returns



True if the specified media behavior is enabled; otherwise, false.




## -remarks



Currently, the only value supported for this function is  <b>MEDIA_BEHAVIOR_MEDIAPLAYBACKLIST_AUTOPLAYBACKITEMRESET</b> which causes media items in a <a href="https://docs.microsoft.com/en-us/uwp/api/Windows.Media.Playback.MediaPlaybackList">MediaPlaybackList</a> to be automatically reset after being played.



