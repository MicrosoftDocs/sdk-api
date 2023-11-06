---
UID: NN:austream.IAudioData
title: IAudioData (austream.h)
description: Note  This interface is deprecated.
helpviewer_keywords: ["IAudioData","IAudioData interface [DirectShow]","IAudioData interface [DirectShow]","described","IAudioDataInterface","austream/IAudioData","dshow.iaudiodata"]
old-location: dshow\iaudiodata.htm
tech.root: dshow
ms.assetid: 8b253715-a294-4e95-b730-e6efe7f895af
ms.date: 4/26/2023
ms.keywords: IAudioData, IAudioData interface [DirectShow], IAudioData interface [DirectShow],described, IAudioDataInterface, austream/IAudioData, dshow.iaudiodata
req.header: austream.h
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
 - IAudioData
 - austream/IAudioData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - austream.h
api_name:
 - IAudioData
---

# IAudioData interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>IAudioData</code> interface provides methods that enable applications to set and get the underlying audio data that audio streams will reference. The audio data format is set in the <a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure.

Implement this interface on underlying audio data objects that audio stream sample objects will access.

Applications use this interface to set and retrieve information on underlying data objects that an audio stream will reference.

## -inheritance

The <b>IAudioData</b> interface inherits from <a href="/windows/desktop/api/austream/nn-austream-imemorydata">IMemoryData</a>. <b>IAudioData</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/austream/nn-austream-imemorydata">IMemoryData</a>
