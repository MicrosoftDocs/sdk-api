---
UID: NS:strmif.tagDVD_PLAYBACK_LOCATION2
title: DVD_PLAYBACK_LOCATION2 (strmif.h)
description: The DVD_PLAYBACK_LOCATION2 structure indicates DVD playback location.
helpviewer_keywords: ["DVD_PLAYBACK_LOCATION2","DVD_PLAYBACK_LOCATION2 structure [DirectShow]","DVD_PLAYBACK_LOCATION2Structure","dshow.dvd_playback_location2","strmif/DVD_PLAYBACK_LOCATION2"]
old-location: dshow\dvd_playback_location2.htm
tech.root: dshow
ms.assetid: 58506709-42e2-43e4-a4c7-b522b7d06e6f
ms.date: 4/26/2023
ms.keywords: DVD_PLAYBACK_LOCATION2, DVD_PLAYBACK_LOCATION2 structure [DirectShow], DVD_PLAYBACK_LOCATION2Structure, dshow.dvd_playback_location2, strmif/DVD_PLAYBACK_LOCATION2
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
targetos: Windows
req.typenames: DVD_PLAYBACK_LOCATION2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDVD_PLAYBACK_LOCATION2
 - strmif/tagDVD_PLAYBACK_LOCATION2
 - DVD_PLAYBACK_LOCATION2
 - strmif/DVD_PLAYBACK_LOCATION2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - DVD_PLAYBACK_LOCATION2
---

# DVD_PLAYBACK_LOCATION2 structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>DVD_PLAYBACK_LOCATION2</code> structure indicates DVD playback location.

## -struct-fields

### -field TitleNum

Title number for the whole disc (not the track number of the Video Title Set).

### -field ChapterNum

Part-of-title number with title. 0xffffffff if not a simple linear movie.

### -field TimeCode

Timecode. Use [DVD_HMSF_TIMECODE](/windows/desktop/api/strmif/ns-strmif-dvd_hmsf_timecode) for current playback time. 0xffffffff if not a simple linear movie.

### -field TimeCodeFlags

A bitwise [DVD_TIMECODE_FLAGS](/windows/desktop/api/strmif/ne-strmif-dvd_timecode_flags) enumeration.

## -remarks

Either <b>TitleNum</b> and <b>ChapterNum</b>, or <b>TitleNum</b> and <b>TimeCode</b>, are sufficient to save the playback location for simple linear movies.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>