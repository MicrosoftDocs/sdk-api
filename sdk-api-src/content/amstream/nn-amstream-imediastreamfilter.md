---
UID: NN:amstream.IMediaStreamFilter
title: IMediaStreamFilter (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The IMediaStreamFilter interface is supported by the Media Stream filter, which is used internally by the multimedia stream object. Applications should not use this interface.
helpviewer_keywords: ["IMediaStreamFilter","IMediaStreamFilter interface [DirectShow]","IMediaStreamFilter interface [DirectShow]","described","IMediaStreamFilterInterface","amstream/IMediaStreamFilter","dshow.imediastreamfilter"]
old-location: dshow\imediastreamfilter.htm
tech.root: dshow
ms.assetid: 1ac4976b-7088-47ac-9689-58c143746f05
ms.date: 4/26/2023
ms.keywords: IMediaStreamFilter, IMediaStreamFilter interface [DirectShow], IMediaStreamFilter interface [DirectShow],described, IMediaStreamFilterInterface, amstream/IMediaStreamFilter, dshow.imediastreamfilter
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
 - IMediaStreamFilter
 - amstream/IMediaStreamFilter
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
 - IMediaStreamFilter
---

# IMediaStreamFilter interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>IMediaStreamFilter</code> interface is supported by the Media Stream filter, which is used internally by the multimedia stream object. Applications should not use this interface.

## -inheritance

The <b>IMediaStreamFilter</b> interface inherits from <a href="/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a>. <b>IMediaStreamFilter</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a>
