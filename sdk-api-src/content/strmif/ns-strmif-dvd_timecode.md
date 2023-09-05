---
UID: NS:strmif.tagDVD_TIMECODE
title: DVD_TIMECODE (strmif.h)
description: The DVD_TIMECODE structure contains DVD timecode in hours, minutes, seconds, and frames.
helpviewer_keywords: ["DVD_TIMECODE","DVD_TIMECODE structure [DirectShow]","DVD_TIMECODEStructure","dshow.dvd_timecode","strmif/DVD_TIMECODE"]
old-location: dshow\dvd_timecode.htm
tech.root: dshow
ms.assetid: 7ad0b11e-5bb7-426f-9a2c-fbc34b2f45b4
ms.date: 4/26/2023
ms.keywords: DVD_TIMECODE, DVD_TIMECODE structure [DirectShow], DVD_TIMECODEStructure, dshow.dvd_timecode, strmif/DVD_TIMECODE
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
req.typenames: DVD_TIMECODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDVD_TIMECODE
 - strmif/tagDVD_TIMECODE
 - DVD_TIMECODE
 - strmif/DVD_TIMECODE
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
 - DVD_TIMECODE
---

# DVD_TIMECODE structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>DVD_TIMECODE</code> structure contains DVD timecode in hours, minutes, seconds, and frames.

## -struct-fields

### -field Hours1

Hours.

### -field Hours10

Tens of hours.

### -field Minutes1

Minutes.

### -field Minutes10

Tens of minutes.

### -field Seconds1

Seconds.

### -field Seconds10

Tens of seconds.

### -field Frames1

Frames.

### -field Frames10

Tens of frames.

### -field FrameRateCode

Frames per second dropped and not dropped as indicated by [DVD_FRAMERATE](/windows/desktop/api/strmif/ne-strmif-dvd_framerate).

## -remarks

DVD timecode is binary coded decimal (BCD) encoded in the format 0xHhMmSsFf, where:

<ul>
<li>H is tens of hours</li>
<li>h is hours</li>
<li>M is tens of minutes</li>
<li>m is minutes</li>
<li>S is tens of seconds</li>
<li>s is seconds</li>
<li>F is tens of frames</li>
<li>f is frames</li>
</ul>

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>