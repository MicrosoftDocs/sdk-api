---
UID: NF:mfplay.IMFPMediaPlayer.GetVideoWindow
title: IMFPMediaPlayer::GetVideoWindow (mfplay.h)
description: Gets the window where the video is displayed.
helpviewer_keywords: ["GetVideoWindow","GetVideoWindow method [Media Foundation]","GetVideoWindow method [Media Foundation]","IMFPMediaPlayer interface","IMFPMediaPlayer interface [Media Foundation]","GetVideoWindow method","IMFPMediaPlayer.GetVideoWindow","IMFPMediaPlayer::GetVideoWindow","mf.imfpmediaplayer_getvideowindow","mfplay/IMFPMediaPlayer::GetVideoWindow"]
old-location: mf\imfpmediaplayer_getvideowindow.htm
tech.root: mf
ms.assetid: 313e3a87-3dad-4cfb-ad37-1018cb03a707
ms.date: 12/05/2018
ms.keywords: GetVideoWindow, GetVideoWindow method [Media Foundation], GetVideoWindow method [Media Foundation],IMFPMediaPlayer interface, IMFPMediaPlayer interface [Media Foundation],GetVideoWindow method, IMFPMediaPlayer.GetVideoWindow, IMFPMediaPlayer::GetVideoWindow, mf.imfpmediaplayer_getvideowindow, mfplay/IMFPMediaPlayer::GetVideoWindow
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
 - IMFPMediaPlayer::GetVideoWindow
 - mfplay/IMFPMediaPlayer::GetVideoWindow
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
 - IMFPMediaPlayer.GetVideoWindow
---

# IMFPMediaPlayer::GetVideoWindow


## -description

<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="/windows/desktop/medfound/media-session">Media Session</a> for playback.</div>
<div> </div>


Gets the window where the video is displayed.

## -parameters

### -param phwndVideo [out]

Receives a handle to the application window where the video is displayed.

## -returns

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.

## -remarks

The video window is specified when you first call <a href="/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer">MFPCreateMediaPlayer</a> to create the MFPlay player object.

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>