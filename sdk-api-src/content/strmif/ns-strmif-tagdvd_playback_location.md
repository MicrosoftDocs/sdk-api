---
UID: NS:strmif.tagDVD_PLAYBACK_LOCATION
title: tagDVD_PLAYBACK_LOCATION
author: windows-sdk-content
description: The DVD_PLAYBACK_LOCATION structure indicates DVD playback location.
old-location: dshow\dvd_playback_location.htm
old-project: DirectShow
ms.assetid: 1085bd1b-ec61-49ca-9c9e-fb090d2a3533
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: DVD_PLAYBACK_LOCATION, DVD_PLAYBACK_LOCATION structure [DirectShow], DVD_PLAYBACK_LOCATIONStructure, dshow.dvd_playback_location, strmif/DVD_PLAYBACK_LOCATION, tagDVD_PLAYBACK_LOCATION
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
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
tech.root: 
req.typenames: DVD_PLAYBACK_LOCATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - DVD_PLAYBACK_LOCATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# tagDVD_PLAYBACK_LOCATION structure


## -description



The <code>DVD_PLAYBACK_LOCATION</code> structure indicates DVD playback location.




## -struct-fields




### -field TitleNum

Title number for the whole disc; Title Track Number (TTN) not Video Title Set_Title Track Number (VTS_TTN).


### -field ChapterNum

Part-of-title number with title. 0xffffffff if not a simple linear movie.


### -field TimeCode

Timecode. Use <a href="https://msdn.microsoft.com/7ad0b11e-5bb7-426f-9a2c-fbc34b2f45b4">DVD_TIMECODE</a> for current playback time. 0xFFFFFFFF if not a simple linear movie.


## -remarks



<b>TitleNum</b> and <b>ChapterNum</b> or <b>TitleNum</b> and <b>TimeCode</b> are sufficient to save the playback location for simple linear movies.




## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

