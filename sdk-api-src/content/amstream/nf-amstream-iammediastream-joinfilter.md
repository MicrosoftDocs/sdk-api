---
UID: NF:amstream.IAMMediaStream.JoinFilter
title: IAMMediaStream::JoinFilter (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The JoinFilter method connects a media stream to the Media Stream filter, which is used internally by the multimedia stream object. Applications should not call this method.
helpviewer_keywords: ["IAMMediaStream interface [DirectShow]","JoinFilter method","IAMMediaStream.JoinFilter","IAMMediaStream::JoinFilter","IAMMediaStreamJoinFilter","JoinFilter","JoinFilter method [DirectShow]","JoinFilter method [DirectShow]","IAMMediaStream interface","amstream/IAMMediaStream::JoinFilter","dshow.iammediastream_joinfilter"]
old-location: dshow\iammediastream_joinfilter.htm
tech.root: dshow
ms.assetid: 638ab6e1-7663-4f15-a487-e22496672ddb
ms.date: 4/26/2023
ms.keywords: IAMMediaStream interface [DirectShow],JoinFilter method, IAMMediaStream.JoinFilter, IAMMediaStream::JoinFilter, IAMMediaStreamJoinFilter, JoinFilter, JoinFilter method [DirectShow], JoinFilter method [DirectShow],IAMMediaStream interface, amstream/IAMMediaStream::JoinFilter, dshow.iammediastream_joinfilter
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
 - IAMMediaStream::JoinFilter
 - amstream/IAMMediaStream::JoinFilter
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
 - IAMMediaStream.JoinFilter
---

# IAMMediaStream::JoinFilter


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>JoinFilter</code> method connects a media stream to the Media Stream filter, which is used internally by the multimedia stream object. Applications should not call this method.

## -parameters

### -param pMediaStreamFilter [in]

Pointer to the filter's <a href="/windows/desktop/api/amstream/nn-amstream-imediastreamfilter">IMediaStreamFilter</a> interface.

## -returns

Returns S_OK if successful.

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-iammediastream">IAMMediaStream Interface</a>