---
UID: NE:strmif.tagDVD_KARAOKE_ASSIGNMENT
title: DVD_KARAOKE_ASSIGNMENT (strmif.h)
description: Defines the speaker configuration for an audio stream.
helpviewer_keywords: ["DVD_Assignment_LR","DVD_Assignment_LR1","DVD_Assignment_LR12","DVD_Assignment_LRM","DVD_Assignment_LRM1","DVD_Assignment_LRM12","DVD_Assignment_reserved0","DVD_Assignment_reserved1","DVD_KARAOKE_ASSIGNMENT","DVD_KARAOKE_ASSIGNMENT","DVD_KARAOKE_ASSIGNMENT enumeration [DirectShow]","DVD_KARAOKE_ASSIGNMENTEnumeration","dshow.dvd_karaoke_assignment","strmif/DVD_Assignment_LR","strmif/DVD_Assignment_LR1","strmif/DVD_Assignment_LR12","strmif/DVD_Assignment_LRM","strmif/DVD_Assignment_LRM1","strmif/DVD_Assignment_LRM12","strmif/DVD_Assignment_reserved0","strmif/DVD_Assignment_reserved1","strmif/DVD_KARAOKE_ASSIGNMENT"]
old-location: dshow\dvd_karaoke_assignment.htm
tech.root: dshow
ms.assetid: cdfd05b9-7a4a-49cc-ab50-bbe83ed9e0f0
ms.date: 4/26/2023
ms.keywords: DVD_Assignment_LR, DVD_Assignment_LR1, DVD_Assignment_LR12, DVD_Assignment_LRM, DVD_Assignment_LRM1, DVD_Assignment_LRM12, DVD_Assignment_reserved0, DVD_Assignment_reserved1, DVD_KARAOKE_ASSIGNMENT, DVD_KARAOKE_ASSIGNMENT , DVD_KARAOKE_ASSIGNMENT enumeration [DirectShow], DVD_KARAOKE_ASSIGNMENTEnumeration, dshow.dvd_karaoke_assignment, strmif/DVD_Assignment_LR, strmif/DVD_Assignment_LR1, strmif/DVD_Assignment_LR12, strmif/DVD_Assignment_LRM, strmif/DVD_Assignment_LRM1, strmif/DVD_Assignment_LRM12, strmif/DVD_Assignment_reserved0, strmif/DVD_Assignment_reserved1, strmif/DVD_KARAOKE_ASSIGNMENT
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
req.typenames: DVD_KARAOKE_ASSIGNMENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDVD_KARAOKE_ASSIGNMENT
 - strmif/tagDVD_KARAOKE_ASSIGNMENT
 - DVD_KARAOKE_ASSIGNMENT
 - strmif/DVD_KARAOKE_ASSIGNMENT
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
 - DVD_KARAOKE_ASSIGNMENT
---

# DVD_KARAOKE_ASSIGNMENT enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Defines the speaker configuration for an audio stream.

## -enum-fields

### -field DVD_Assignment_reserved0:0

Reserved.

### -field DVD_Assignment_reserved1:1

Reserved.

### -field DVD_Assignment_LR:2

The stream is assigned to the left and right speakers.

### -field DVD_Assignment_LRM:3

The stream is assigned to the left, right, and middle speakers.

### -field DVD_Assignment_LR1:4

The stream is assigned to the left, right, and audio1 speakers.

### -field DVD_Assignment_LRM1:5

The stream is assigned to the left, right, middle, and audio1 speakers.

### -field DVD_Assignment_LR12:6

The stream is assigned to the left, right, and audio2 speakers.

### -field DVD_Assignment_LRM12:7

The stream is assigned to the left, right, middle, and audio2 speakers.

## -remarks

All channels within a stream will use the same speaker configuration, although the channels can be sent to different speakers within this configuration.

## -see-also

[DVD_KaraokeAttributes Structure](/windows/desktop/api/strmif/ns-strmif-dvd_karaokeattributes)



<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>
