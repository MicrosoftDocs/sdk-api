---
UID: NF:mfplay.IMFPMediaItem.GetMediaPlayer
title: IMFPMediaItem::GetMediaPlayer (mfplay.h)
description: Gets a pointer to the MFPlay player object that created the media item.
helpviewer_keywords: ["GetMediaPlayer","GetMediaPlayer method [Media Foundation]","GetMediaPlayer method [Media Foundation]","IMFPMediaItem interface","IMFPMediaItem interface [Media Foundation]","GetMediaPlayer method","IMFPMediaItem.GetMediaPlayer","IMFPMediaItem::GetMediaPlayer","mf.imfpmediaitem_getmediaplayer","mfplay/IMFPMediaItem::GetMediaPlayer"]
old-location: mf\imfpmediaitem_getmediaplayer.htm
tech.root: mf
ms.assetid: 6d6f822a-d599-437e-a73a-2242d4d3fe3a
ms.date: 12/05/2018
ms.keywords: GetMediaPlayer, GetMediaPlayer method [Media Foundation], GetMediaPlayer method [Media Foundation],IMFPMediaItem interface, IMFPMediaItem interface [Media Foundation],GetMediaPlayer method, IMFPMediaItem.GetMediaPlayer, IMFPMediaItem::GetMediaPlayer, mf.imfpmediaitem_getmediaplayer, mfplay/IMFPMediaItem::GetMediaPlayer
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
 - IMFPMediaItem::GetMediaPlayer
 - mfplay/IMFPMediaItem::GetMediaPlayer
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
 - IMFPMediaItem.GetMediaPlayer
---

# IMFPMediaItem::GetMediaPlayer


## -description

<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="/windows/desktop/medfound/media-session">Media Session</a> for playback.</div>
<div> </div>


Gets a pointer to the MFPlay player object that created the media item.

## -parameters

### -param ppMediaPlayer [out]

Receives a pointer to the player object's <a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a> interface. The caller must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem">IMFPMediaItem</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>