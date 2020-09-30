---
UID: NF:mfplay.IMFPMediaItem.GetUserData
title: IMFPMediaItem::GetUserData (mfplay.h)
description: Gets the application-defined value stored in the media item.
helpviewer_keywords: ["GetUserData","GetUserData method [Media Foundation]","GetUserData method [Media Foundation]","IMFPMediaItem interface","IMFPMediaItem interface [Media Foundation]","GetUserData method","IMFPMediaItem.GetUserData","IMFPMediaItem::GetUserData","mf.imfpmediaitem_getuserdata","mfplay/IMFPMediaItem::GetUserData"]
old-location: mf\imfpmediaitem_getuserdata.htm
tech.root: mf
ms.assetid: aa99ced1-c32b-4bf5-b29a-e16eceddfed1
ms.date: 12/05/2018
ms.keywords: GetUserData, GetUserData method [Media Foundation], GetUserData method [Media Foundation],IMFPMediaItem interface, IMFPMediaItem interface [Media Foundation],GetUserData method, IMFPMediaItem.GetUserData, IMFPMediaItem::GetUserData, mf.imfpmediaitem_getuserdata, mfplay/IMFPMediaItem::GetUserData
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
 - IMFPMediaItem::GetUserData
 - mfplay/IMFPMediaItem::GetUserData
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
 - IMFPMediaItem.GetUserData
---

# IMFPMediaItem::GetUserData


## -description

<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="/windows/desktop/medfound/media-session">Media Session</a> for playback.</div>
<div> </div>


Gets the application-defined value stored in the media item.

## -parameters

### -param pdwUserData [out]

Receives the application-defined value for the media item.

## -returns

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.

## -remarks

You can assign this value when you first create the media item, by specifying it in the <i>dwUserData</i> parameter of the <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl">IMFPMediaPlayer::CreateMediaItemFromURL</a> or <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject">IMFPMediaPlayer::CreateMediaItemFromObject</a> method. To update the value, call <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-setuserdata">IMFPMediaItem::SetUserData</a>.

This method can be called after the player object is shut down.

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem">IMFPMediaItem</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>