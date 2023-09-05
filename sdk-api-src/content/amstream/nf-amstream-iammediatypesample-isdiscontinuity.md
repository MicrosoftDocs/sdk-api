---
UID: NF:amstream.IAMMediaTypeSample.IsDiscontinuity
title: IAMMediaTypeSample::IsDiscontinuity (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The IsDiscontinuity method determines if this sample represents a discontinuity in the data stream.
helpviewer_keywords: ["IAMMediaTypeSample interface [DirectShow]","IsDiscontinuity method","IAMMediaTypeSample.IsDiscontinuity","IAMMediaTypeSample::IsDiscontinuity","IAMMediaTypeSampleIsDiscontinuity","IsDiscontinuity","IsDiscontinuity method [DirectShow]","IsDiscontinuity method [DirectShow]","IAMMediaTypeSample interface","amstream/IAMMediaTypeSample::IsDiscontinuity","dshow.iammediatypesample_isdiscontinuity"]
old-location: dshow\iammediatypesample_isdiscontinuity.htm
tech.root: dshow
ms.assetid: 857729d9-ef46-461b-a3b5-bce9acb84538
ms.date: 4/26/2023
ms.keywords: IAMMediaTypeSample interface [DirectShow],IsDiscontinuity method, IAMMediaTypeSample.IsDiscontinuity, IAMMediaTypeSample::IsDiscontinuity, IAMMediaTypeSampleIsDiscontinuity, IsDiscontinuity, IsDiscontinuity method [DirectShow], IsDiscontinuity method [DirectShow],IAMMediaTypeSample interface, amstream/IAMMediaTypeSample::IsDiscontinuity, dshow.iammediatypesample_isdiscontinuity
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
 - IAMMediaTypeSample::IsDiscontinuity
 - amstream/IAMMediaTypeSample::IsDiscontinuity
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
 - IAMMediaTypeSample.IsDiscontinuity
---

# IAMMediaTypeSample::IsDiscontinuity


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>IsDiscontinuity</code> method determines if this sample represents a discontinuity in the data stream.



## -returns

Returns S_OK if this sample is a discontinuity, or S_FALSE otherwise.

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-iammediatypesample">IAMMediaTypeSample Interface</a>
