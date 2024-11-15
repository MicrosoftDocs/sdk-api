---
UID: NN:mfplay.IMFPMediaPlayerCallback
title: IMFPMediaPlayerCallback (mfplay.h)
description: Callback interface for the IMFPMediaPlayer interface.
helpviewer_keywords: ["IMFPMediaPlayerCallback","IMFPMediaPlayerCallback interface [Media Foundation]","IMFPMediaPlayerCallback interface [Media Foundation]","described","mf.imfpmediaplayercallback","mfplay/IMFPMediaPlayerCallback"]
old-location: mf\imfpmediaplayercallback.htm
tech.root: mfarchive
archived: true
ms.assetid: 7d9d01bf-861a-4c35-93b1-dbf85cbf0a32
ms.date: 12/05/2018
ms.keywords: IMFPMediaPlayerCallback, IMFPMediaPlayerCallback interface [Media Foundation], IMFPMediaPlayerCallback interface [Media Foundation],described, mf.imfpmediaplayercallback, mfplay/IMFPMediaPlayerCallback
req.header: mfplay.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IMFPMediaPlayerCallback
 - mfplay/IMFPMediaPlayerCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplay.h
api_name:
 - IMFPMediaPlayerCallback
---

# IMFPMediaPlayerCallback interface


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Callback interface for the <a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a> interface.

To set the callback, pass an <b>IMFPMediaPlayerCallback</b> pointer to the <a href="/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer">MFPCreateMediaPlayer</a>  function in the  <i>pCallback</i>  parameter. The application implements the <b>IMFPMediaPlayerCallback</b> interface.

## -inheritance

The <b>IMFPMediaPlayerCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFPMediaPlayerCallback</b> also has these types of members:

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>
