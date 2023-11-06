---
UID: NS:strmif.tagDVD_KaraokeAttributes
title: DVD_KaraokeAttributes (strmif.h)
description: The DVD_KaraokeAttributes structure contains information about a karaoke audio stream. The IDvdInfo2::GetKaraokeAttributes method fills in a DVD_KaraokeAttributes structure for a specified stream.
helpviewer_keywords: ["DVD_KaraokeAttributes","DVD_KaraokeAttributes structure [DirectShow]","DVD_KaraokeAttributesStructure","dshow.dvd_karaokeattributes","strmif/DVD_KaraokeAttributes"]
old-location: dshow\dvd_karaokeattributes.htm
tech.root: dshow
ms.assetid: dffb0b0e-edce-47e7-b9c0-983fdd2c4746
ms.date: 4/26/2023
ms.keywords: DVD_KaraokeAttributes, DVD_KaraokeAttributes structure [DirectShow], DVD_KaraokeAttributesStructure, dshow.dvd_karaokeattributes, strmif/DVD_KaraokeAttributes
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
req.typenames: DVD_KaraokeAttributes
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDVD_KaraokeAttributes
 - strmif/tagDVD_KaraokeAttributes
 - DVD_KaraokeAttributes
 - strmif/DVD_KaraokeAttributes
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
 - DVD_KaraokeAttributes
---

# DVD_KaraokeAttributes structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>DVD_KaraokeAttributes</code> structure contains information about a karaoke audio stream. The <a href="/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getkaraokeattributes">IDvdInfo2::GetKaraokeAttributes</a> method fills in a <code>DVD_KaraokeAttributes</code> structure for a specified stream.

## -struct-fields

### -field bVersion

Version number. The current karaoke version is 1.0.

### -field fMasterOfCeremoniesInGuideVocal1

If <b>TRUE</b>, the "Guide Vocal 1" channel contains the "Master of Ceremonies" content.

### -field fDuet

A Boolean value indicating whether the song is intended to be sung as a duet.

### -field ChannelAssignment

A [DVD_KARAOKE_ASSIGNMENT](/windows/win32/api/strmif/ne-strmif-dvd_karaoke_assignment) value indicating the speaker configuration into which all the channels will be mixed.

### -field wChannelContents

An array of valid [DVD_KARAOKE_CONTENTS](/windows/desktop/api/strmif/ne-strmif-dvd_karaoke_contents) values that identifies the content on each channel.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>