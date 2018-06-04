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

# tagDVD_PLAYBACK_LOCATION2 structure


## -description



The <code>DVD_PLAYBACK_LOCATION2</code> structure indicates DVD playback location.




## -struct-fields




### -field TitleNum

Title number for the whole disc (not the track number of the Video Title Set).


### -field ChapterNum

Part-of-title number with title. 0xffffffff if not a simple linear movie.


### -field TimeCode

Timecode. Use <a href="https://msdn.microsoft.com/8f2990f6-a8f5-4b16-ae30-d51ea55496ea">DVD_HMSF_TIMECODE</a> for current playback time. 0xffffffff if not a simple linear movie.


### -field TimeCodeFlags

A bitwise <b>OR</b> of flags from the <a href="https://msdn.microsoft.com/2dc5ce97-12a4-43a0-b897-14fea32d8efc">DVD_TIMECODE_FLAGS</a> enumeration.


## -remarks



Either <b>TitleNum</b> and <b>ChapterNum</b>, or <b>TitleNum</b> and <b>TimeCode</b>, are sufficient to save the playback location for simple linear movies.




## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

