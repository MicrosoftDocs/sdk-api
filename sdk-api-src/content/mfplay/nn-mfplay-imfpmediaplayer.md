---
UID: NN:mfplay.IMFPMediaPlayer
title: IMFPMediaPlayer (mfplay.h)
description: Contains methods to play media files. (Deprecated.).
helpviewer_keywords: ["IMFPMediaPlayer","IMFPMediaPlayer interface [Media Foundation]","IMFPMediaPlayer interface [Media Foundation]","described","mf.imfpmediaplayer","mfplay/IMFPMediaPlayer"]
old-location: mf\imfpmediaplayer.htm
tech.root: mfarchive
archived: true
ms.assetid: fa57d465-1ee9-4f7a-9be8-66a6d73f65e8
ms.date: 12/05/2018
ms.keywords: IMFPMediaPlayer, IMFPMediaPlayer interface [Media Foundation], IMFPMediaPlayer interface [Media Foundation],described, mf.imfpmediaplayer, mfplay/IMFPMediaPlayer
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
 - IMFPMediaPlayer
 - mfplay/IMFPMediaPlayer
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
 - IMFPMediaPlayer
---

# IMFPMediaPlayer interface


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Contains methods to play media files.

The MFPlay player object exposes this interface. To get a pointer to this interface, call <a href="/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer">MFPCreateMediaPlayer</a>.

## -inheritance

The <b>IMFPMediaPlayer</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFPMediaPlayer</b> also has these types of members:

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>
