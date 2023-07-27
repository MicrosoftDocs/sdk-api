---
UID: NF:amstream.IAMMediaTypeSample.SetDiscontinuity
title: IAMMediaTypeSample::SetDiscontinuity (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The SetDiscontinuity method sets the discontinuity property.
helpviewer_keywords: ["IAMMediaTypeSample interface [DirectShow]","SetDiscontinuity method","IAMMediaTypeSample.SetDiscontinuity","IAMMediaTypeSample::SetDiscontinuity","IAMMediaTypeSampleSetDiscontinuity","SetDiscontinuity","SetDiscontinuity method [DirectShow]","SetDiscontinuity method [DirectShow]","IAMMediaTypeSample interface","amstream/IAMMediaTypeSample::SetDiscontinuity","dshow.iammediatypesample_setdiscontinuity"]
old-location: dshow\iammediatypesample_setdiscontinuity.htm
tech.root: dshow
ms.assetid: 9dcac2ce-c9a0-40be-aa86-b4acbd4d06a7
ms.date: 4/26/2023
ms.keywords: IAMMediaTypeSample interface [DirectShow],SetDiscontinuity method, IAMMediaTypeSample.SetDiscontinuity, IAMMediaTypeSample::SetDiscontinuity, IAMMediaTypeSampleSetDiscontinuity, SetDiscontinuity, SetDiscontinuity method [DirectShow], SetDiscontinuity method [DirectShow],IAMMediaTypeSample interface, amstream/IAMMediaTypeSample::SetDiscontinuity, dshow.iammediatypesample_setdiscontinuity
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
 - IAMMediaTypeSample::SetDiscontinuity
 - amstream/IAMMediaTypeSample::SetDiscontinuity
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
 - IAMMediaTypeSample.SetDiscontinuity
---

# IAMMediaTypeSample::SetDiscontinuity


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>SetDiscontinuity</code> method sets the discontinuity property.

## -parameters

### -param bDiscontinuity

Value that specifies whether this sample is a discontinuity. If the sample is discontinuous with the previous sample, set the value to <b>TRUE</b>. Otherwise, set the value to <b>FALSE</b>.

## -returns

Returns S_OK.

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-iammediatypesample">IAMMediaTypeSample Interface</a>