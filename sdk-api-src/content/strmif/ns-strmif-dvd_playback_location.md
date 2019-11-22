---
UID: NS:strmif.tagDVD_PLAYBACK_LOCATION
title: DVD_PLAYBACK_LOCATION (strmif.h)

description: The DVD_PLAYBACK_LOCATION structure indicates DVD playback location.
old-location: dshow\dvd_playback_location.htm
tech.root: DirectShow
ms.assetid: 1085bd1b-ec61-49ca-9c9e-fb090d2a3533

ms.date: 12/05/2018
ms.keywords: DVD_PLAYBACK_LOCATION, DVD_PLAYBACK_LOCATION structure [DirectShow], DVD_PLAYBACK_LOCATIONStructure, dshow.dvd_playback_location, strmif/DVD_PLAYBACK_LOCATION
ms.topic: struct
f1_keywords: 
 - "strmif/DVD_PLAYBACK_LOCATION"
dev_langs:
 - c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - DVD_PLAYBACK_LOCATION
targetos: Windows
req.typenames: DVD_PLAYBACK_LOCATION
req.redist: 
ms.custom: 19H1
---

# DVD_PLAYBACK_LOCATION structure


## -description



The <code>DVD_PLAYBACK_LOCATION</code> structure indicates DVD playback location.




## -struct-fields




### -field TitleNum

Title number for the whole disc; Title Track Number (TTN) not Video Title Set_Title Track Number (VTS_TTN).


### -field ChapterNum

Part-of-title number with title. 0xffffffff if not a simple linear movie.


### -field TimeCode

Timecode. Use <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ns-strmif-dvd_timecode">DVD_TIMECODE</a> for current playback time. 0xFFFFFFFF if not a simple linear movie.


## -remarks



<b>TitleNum</b> and <b>ChapterNum</b> or <b>TitleNum</b> and <b>TimeCode</b> are sufficient to save the playback location for simple linear movies.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>
 

 

