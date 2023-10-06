---
UID: NE:strmif.tagDVD_AUDIO_FORMAT
title: DVD_AUDIO_FORMAT (strmif.h)
description: Indicates the audio format of a DVD.
helpviewer_keywords: ["DVD_AUDIO_FORMAT","DVD_AUDIO_FORMAT","DVD_AUDIO_FORMAT enumeration [DirectShow]","DVD_AUDIO_FORMATEnumeration","DVD_AudioFormat_AC3","DVD_AudioFormat_DTS","DVD_AudioFormat_LPCM","DVD_AudioFormat_MPEG1","DVD_AudioFormat_MPEG1_DRC","DVD_AudioFormat_MPEG2","DVD_AudioFormat_MPEG2_DRC","DVD_AudioFormat_Other","DVD_AudioFormat_SDDS","dshow.dvd_audio_format","strmif/DVD_AUDIO_FORMAT","strmif/DVD_AudioFormat_AC3","strmif/DVD_AudioFormat_DTS","strmif/DVD_AudioFormat_LPCM","strmif/DVD_AudioFormat_MPEG1","strmif/DVD_AudioFormat_MPEG1_DRC","strmif/DVD_AudioFormat_MPEG2","strmif/DVD_AudioFormat_MPEG2_DRC","strmif/DVD_AudioFormat_Other","strmif/DVD_AudioFormat_SDDS"]
old-location: dshow\dvd_audio_format.htm
tech.root: dshow
ms.assetid: 99fffd6b-a37f-4dac-8849-0409caba3c13
ms.date: 4/26/2023
ms.keywords: DVD_AUDIO_FORMAT, DVD_AUDIO_FORMAT , DVD_AUDIO_FORMAT enumeration [DirectShow], DVD_AUDIO_FORMATEnumeration, DVD_AudioFormat_AC3, DVD_AudioFormat_DTS, DVD_AudioFormat_LPCM, DVD_AudioFormat_MPEG1, DVD_AudioFormat_MPEG1_DRC, DVD_AudioFormat_MPEG2, DVD_AudioFormat_MPEG2_DRC, DVD_AudioFormat_Other, DVD_AudioFormat_SDDS, dshow.dvd_audio_format, strmif/DVD_AUDIO_FORMAT, strmif/DVD_AudioFormat_AC3, strmif/DVD_AudioFormat_DTS, strmif/DVD_AudioFormat_LPCM, strmif/DVD_AudioFormat_MPEG1, strmif/DVD_AudioFormat_MPEG1_DRC, strmif/DVD_AudioFormat_MPEG2, strmif/DVD_AudioFormat_MPEG2_DRC, strmif/DVD_AudioFormat_Other, strmif/DVD_AudioFormat_SDDS
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
req.typenames: DVD_AUDIO_FORMAT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDVD_AUDIO_FORMAT
 - strmif/tagDVD_AUDIO_FORMAT
 - DVD_AUDIO_FORMAT
 - strmif/DVD_AUDIO_FORMAT
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
 - DVD_AUDIO_FORMAT
---

# DVD_AUDIO_FORMAT enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Indicates the audio format of a DVD.

## -enum-fields

### -field DVD_AudioFormat_AC3:0

Audio format is Dolby AC-3.

### -field DVD_AudioFormat_MPEG1:1

Audio format is MPEG-1.

### -field DVD_AudioFormat_MPEG1_DRC:2

Audio format is MPEG-1 with dynamic range control.

### -field DVD_AudioFormat_MPEG2:3

Audio format is MPEG-2.

### -field DVD_AudioFormat_MPEG2_DRC:4

Audio format is MPEG-2 with dynamic range control.

### -field DVD_AudioFormat_LPCM:5

Audio format is Linear Pulse Code Modulated (LPCM).

### -field DVD_AudioFormat_DTS:6

Audio format is Digital Theater Systems (DTS).

### -field DVD_AudioFormat_SDDS:7

Audio format is Sony Dynamic Digital Sound (SDDS).

### -field DVD_AudioFormat_Other:8

Audio format is unrecognized.

## -remarks

This enumeration is a member of the [DVD_AudioAttributes](/windows/desktop/api/strmif/ns-strmif-dvd_audioattributes) structure.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>
