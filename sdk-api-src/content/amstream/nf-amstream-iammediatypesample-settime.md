---
UID: NF:amstream.IAMMediaTypeSample.SetTime
title: IAMMediaTypeSample::SetTime (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The SetTime method sets the stream times at which the sample should start and stop.
helpviewer_keywords: ["IAMMediaTypeSample interface [DirectShow]","SetTime method","IAMMediaTypeSample.SetTime","IAMMediaTypeSample::SetTime","IAMMediaTypeSampleSetTime","SetTime","SetTime method [DirectShow]","SetTime method [DirectShow]","IAMMediaTypeSample interface","amstream/IAMMediaTypeSample::SetTime","dshow.iammediatypesample_settime"]
old-location: dshow\iammediatypesample_settime.htm
tech.root: dshow
ms.assetid: b8f2c1bd-ea78-43b8-881c-d1f1a64ee575
ms.date: 4/26/2023
ms.keywords: IAMMediaTypeSample interface [DirectShow],SetTime method, IAMMediaTypeSample.SetTime, IAMMediaTypeSample::SetTime, IAMMediaTypeSampleSetTime, SetTime, SetTime method [DirectShow], SetTime method [DirectShow],IAMMediaTypeSample interface, amstream/IAMMediaTypeSample::SetTime, dshow.iammediatypesample_settime
req.header: amstream.h
req.include-header: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMMediaTypeSample::SetTime
 - amstream/IAMMediaTypeSample::SetTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - amstream.h
api_name:
 - IAMMediaTypeSample.SetTime
---

# IAMMediaTypeSample::SetTime


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>SetTime</code> method sets the stream times at which the sample should start and stop.

## -parameters

### -param pTimeStart [in]

Pointer to a variable that contains the start time.

### -param pTimeEnd [in]

Pointer to a variable that contains the stop time.

## -returns

Returns S_OK.

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-iammediatypesample">IAMMediaTypeSample Interface</a>