---
UID: NE:strmif.tagDVD_FRAMERATE
title: DVD_FRAMERATE (strmif.h)
description: Indicates whether the DVD is authored to play at 25 or 30 frames per second.
helpviewer_keywords: ["DVD_FPS_25","DVD_FPS_30NonDrop","DVD_FRAMERATE","DVD_FRAMERATE","DVD_FRAMERATE enumeration [DirectShow]","DVD_FRAMERATEEnumeration","dshow.dvd_framerate","strmif/DVD_FPS_25","strmif/DVD_FPS_30NonDrop","strmif/DVD_FRAMERATE"]
old-location: dshow\dvd_framerate.htm
tech.root: dshow
ms.assetid: 92309c56-87fe-43cc-b76e-43f9686177be
ms.date: 12/05/2018
ms.keywords: DVD_FPS_25, DVD_FPS_30NonDrop, DVD_FRAMERATE, DVD_FRAMERATE , DVD_FRAMERATE enumeration [DirectShow], DVD_FRAMERATEEnumeration, dshow.dvd_framerate, strmif/DVD_FPS_25, strmif/DVD_FPS_30NonDrop, strmif/DVD_FRAMERATE
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
req.typenames: DVD_FRAMERATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDVD_FRAMERATE
 - strmif/tagDVD_FRAMERATE
 - DVD_FRAMERATE
 - strmif/DVD_FRAMERATE
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
 - DVD_FRAMERATE
---

# DVD_FRAMERATE enumeration


## -description

Indicates whether the DVD is authored to play at 25 or 30 frames per second.

## -enum-fields

### -field DVD_FPS_25:1

Twenty-five frames per second.

### -field DVD_FPS_30NonDrop:3

Exactly 30 frames per second.

## -remarks

You must know the frame rate to interpret the frame count as time.

## -see-also

[DVD_TIMECODE](/windows/desktop/api/strmif/ns-strmif-dvd_timecode)



<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>
