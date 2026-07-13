---
UID: NN:mfplay.IMFPMediaItem
title: IMFPMediaItem (mfplay.h)
description: Represents a media item. (Deprecated.).
helpviewer_keywords: ["IMFPMediaItem","IMFPMediaItem interface [Media Foundation]","IMFPMediaItem interface [Media Foundation]","described","mf.imfpmediaitem","mfplay/IMFPMediaItem"]
old-location: mf\imfpmediaitem.htm
tech.root: mfarchive
archived: true
ms.assetid: 2839d256-bdaf-40cf-9f9d-46f9e2ce59e8
ms.date: 12/05/2018
ms.keywords: IMFPMediaItem, IMFPMediaItem interface [Media Foundation], IMFPMediaItem interface [Media Foundation],described, mf.imfpmediaitem, mfplay/IMFPMediaItem
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
 - IMFPMediaItem
 - mfplay/IMFPMediaItem
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
 - IMFPMediaItem
---

# IMFPMediaItem interface


## -description

<div class="alert"><b>Note</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="/windows/desktop/medfound/media-session">Media Session</a> for playback.</div>
<div> </div>


Represents a media item. A <i>media item</i> is an abstraction for a source of media data, such as a video file. Use this interface to get information about the source, or to change certain playback settings, such as the start and stop times. To get a pointer to this interface, call one of the following methods:
<ul>
<li>
<a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject">IMFPMediaPlayer::CreateMediaItemFromObject</a>
</li>
<li>
<a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl">IMFPMediaPlayer::CreateMediaItemFromURL</a>
</li>
</ul>

## -inheritance

The <b>IMFPMediaItem</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFPMediaItem</b> also has these types of members:

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>
