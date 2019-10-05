---
UID: NF:mfplay.IMFPMediaPlayer.ClearMediaItem
title: IMFPMediaPlayer::ClearMediaItem (mfplay.h)
author: windows-sdk-content
description: Clears the current media item.
old-location: mf\imfpmediaplayer_clearmediaitem.htm
tech.root: medfound
ms.assetid: 2c2b23ab-b282-445f-a5a0-4291ee6f22ba
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ClearMediaItem, ClearMediaItem method [Media Foundation], ClearMediaItem method [Media Foundation],IMFPMediaPlayer interface, IMFPMediaPlayer interface [Media Foundation],ClearMediaItem method, IMFPMediaPlayer.ClearMediaItem, IMFPMediaPlayer::ClearMediaItem, mf.imfpmediaplayer_clearmediaitem, mfplay/IMFPMediaPlayer::ClearMediaItem
ms.topic: method
f1_keywords: 
 - "mfplay/IMFPMediaPlayer.ClearMediaItem"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplay.h
api_name:
 - IMFPMediaPlayer.ClearMediaItem
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFPMediaPlayer::ClearMediaItem


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://docs.microsoft.com/windows/desktop/medfound/media-session">Media Session</a> for playback.</div>
<div> </div>


Clears the current media item.
<div class="alert"><b>Note</b>  This method is currently not implemented.</div><div> </div>

## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method stops playback and releases the player object's references to the current media item.

This method completes asynchronously.  When the operation completes, the application's <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent">IMFPMediaPlayerCallback::OnMediaPlayerEvent</a> callback method is invoked. The event type is <b>MFP_EVENT_TYPE_MEDIAITEM_CLEARED</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>
 

 

