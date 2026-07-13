---
UID: NF:mfplay.MFPCreateMediaPlayer
title: MFPCreateMediaPlayer function (mfplay.h)
description: Creates a new instance of the MFPlay player object.
helpviewer_keywords: ["MFPCreateMediaPlayer","MFPCreateMediaPlayer function [Media Foundation]","mf.mfpcreatemediaplayer","mfplay/MFPCreateMediaPlayer"]
old-location: mf\mfpcreatemediaplayer.htm
tech.root: mfarchive
archived: true
ms.assetid: 80c668e2-5e93-4af2-871c-646228e18717
ms.date: 12/05/2018
ms.keywords: MFPCreateMediaPlayer, MFPCreateMediaPlayer function [Media Foundation], mf.mfpcreatemediaplayer, mfplay/MFPCreateMediaPlayer
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
req.lib: Mfplay.lib
req.dll: Mfplay.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFPCreateMediaPlayer
 - mfplay/MFPCreateMediaPlayer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplay.dll
api_name:
 - MFPCreateMediaPlayer
---

# MFPCreateMediaPlayer function


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Creates a new instance of the MFPlay player object.

## -parameters

### -param pwszURL [in]

Null-terminated string that contains the URL  of a media file to open. This parameter can be <b>NULL</b>. If the parameter is <b>NULL</b>, <i>fStartPlayback</i> must be <b>FALSE</b>.

If this parameter is <b>NULL</b>, you can open a URL later by calling <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl">IMFPMediaPlayer::CreateMediaItemFromURL</a>.

### -param fStartPlayback [in]

If <b>TRUE</b>, playback starts automatically. If <b>FALSE</b>, playback does not start until the application calls <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play">IMFMediaPlayer::Play</a>.

If <i>pwszURL</i> is <b>NULL</b>, this parameter is ignored.

### -param creationOptions [in]

Bitwise <b>OR</b> of zero of more flags from the <a href="/windows/win32/api/mfplay/ne-mfplay-_mfp_creation_options">_MFP_CREATION_OPTIONS</a> enumeration.

### -param pCallback [in]

Pointer to the <a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback">IMFPMediaPlayerCallback</a> interface of a callback object, implemented by the application. Use this interface to get event notifications from the MFPlay player object. This parameter can be <b>NULL</b>. If  the parameter is <b>NULL</b>, the application will not receive  event notifications from the player object.

### -param hWnd [in]

A handle to a window where the video will appear. For audio-only playback, this parameter can be <b>NULL</b>.

The window specified by <i>hWnd</i> is used for the first selected video stream in the source. If the source has multiple video streams, you must call <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-setstreamsink">IMFPMediaItem::SetStreamSink</a> to render any of the video streams after the first.

If <i>hWnd</i> is <b>NULL</b>, MFPlay will not display any video unless the application calls <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-setstreamsink">IMFPMediaItem::SetStreamSink</a> to specify a media sink for the video stream.

### -param ppMediaPlayer [out]

Receives a pointer to the <a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a> interface. The caller must release the interface. This parameter can be <b>NULL</b>. If this parameter is <b>NULL</b>, <i>fStartPlayback</i> must be <b>TRUE</b> and <i>pwszURL</i> cannot be <b>NULL</b>.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Before calling this function, call <b>CoIntialize(Ex)</b> from the same thread to initialize the COM library.

Internally, <b>MFPCreateMediaPlayer</b> calls <a href="/windows/desktop/api/mfapi/nf-mfapi-mfstartup">MFStartup</a> to initialize the Microsoft Media Foundation platform. When the player object is destroyed, it calls  <a href="/windows/desktop/api/mfapi/nf-mfapi-mfshutdown">MFShutdown</a> to shut down the platform. It is not necessary for an application to call <b>MFStartup</b> or <b>MFShutdown</b> when using MFPlay.

<div class="alert"><b>Note</b>  If you use other Media Foundation APIs outside the life time of the player object, then your application should call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfstartup">MFStartup</a> and <a href="/windows/desktop/api/mfapi/nf-mfapi-mfshutdown">MFShutdown</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>