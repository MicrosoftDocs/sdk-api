---
UID: NF:amstream.IAMMediaStream.SetState
title: IAMMediaStream::SetState (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The SetState method sets the filter state.
helpviewer_keywords: ["IAMMediaStream interface [DirectShow]","SetState method","IAMMediaStream.SetState","IAMMediaStream::SetState","IAMMediaStreamSetState","SetState","SetState method [DirectShow]","SetState method [DirectShow]","IAMMediaStream interface","amstream/IAMMediaStream::SetState","dshow.iammediastream_setstate"]
old-location: dshow\iammediastream_setstate.htm
tech.root: dshow
ms.assetid: 2134c2cf-4d78-438c-8fb9-a96f87f682d9
ms.date: 4/26/2023
ms.keywords: IAMMediaStream interface [DirectShow],SetState method, IAMMediaStream.SetState, IAMMediaStream::SetState, IAMMediaStreamSetState, SetState, SetState method [DirectShow], SetState method [DirectShow],IAMMediaStream interface, amstream/IAMMediaStream::SetState, dshow.iammediastream_setstate
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
 - IAMMediaStream::SetState
 - amstream/IAMMediaStream::SetState
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
 - IAMMediaStream.SetState
---

# IAMMediaStream::SetState


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>SetState</code> method sets the filter state.

## -parameters

### -param State [in]

Sets the filter's state, as specified by the <a href="/windows/win32/api/strmif/ne-strmif-filter_state">FILTER_STATE</a> enumerated type.

## -returns

Returns S_OK if successful or E_INVALIDARG if the <i>State</i> parameter is invalid.

## -remarks

Applications should not call this method.

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-iammediastream">IAMMediaStream Interface</a>