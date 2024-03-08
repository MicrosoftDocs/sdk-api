---
UID: NN:mediaobj.IMediaBuffer
title: IMediaBuffer (mediaobj.h)
description: The IMediaBuffer interface provides methods for manipulating a data buffer. Buffers passed to the IMediaObject::ProcessInput and ProcessOutput methods must implement this interface.
helpviewer_keywords: ["IMediaBuffer","IMediaBuffer interface [DirectShow]","IMediaBuffer interface [DirectShow]","described","IMediaBufferInterface","dshow.imediabuffer","mediaobj/IMediaBuffer"]
old-location: dshow\imediabuffer.htm
tech.root: dshow
ms.assetid: 74d72ca6-f899-43fc-bdea-5208d920f314
ms.date: 4/26/2023
ms.keywords: IMediaBuffer, IMediaBuffer interface [DirectShow], IMediaBuffer interface [DirectShow],described, IMediaBufferInterface, dshow.imediabuffer, mediaobj/IMediaBuffer
req.header: mediaobj.h
req.include-header: Dmo.h
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
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMediaBuffer
 - mediaobj/IMediaBuffer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IMediaBuffer
---

# IMediaBuffer interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IMediaBuffer</code> interface provides methods for manipulating a data buffer. Buffers passed to the <b>IMediaObject::ProcessInput</b> and <b>ProcessOutput</b> methods must implement this interface.

## -inheritance

The <b>IMediaBuffer</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMediaBuffer</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/DirectShow/implementing-imediabuffer">Implementing IMediaBuffer</a>
