---
UID: NF:mfplay.IMFPMediaPlayer.SetMediaItem
title: IMFPMediaPlayer::SetMediaItem (mfplay.h)
description: Queues a media item for playback.
helpviewer_keywords: ["IMFPMediaPlayer interface [Media Foundation]","SetMediaItem method","IMFPMediaPlayer.SetMediaItem","IMFPMediaPlayer::SetMediaItem","SetMediaItem","SetMediaItem method [Media Foundation]","SetMediaItem method [Media Foundation]","IMFPMediaPlayer interface","mf.imfpmediaplayer_setmediaitem","mfplay/IMFPMediaPlayer::SetMediaItem"]
old-location: mf\imfpmediaplayer_setmediaitem.htm
tech.root: mfarchive
archived: true
ms.assetid: c792a024-c4f8-4e0b-9720-259d1dc28ee8
ms.date: 12/05/2018
ms.keywords: IMFPMediaPlayer interface [Media Foundation],SetMediaItem method, IMFPMediaPlayer.SetMediaItem, IMFPMediaPlayer::SetMediaItem, SetMediaItem, SetMediaItem method [Media Foundation], SetMediaItem method [Media Foundation],IMFPMediaPlayer interface, mf.imfpmediaplayer_setmediaitem, mfplay/IMFPMediaPlayer::SetMediaItem
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
 - IMFPMediaPlayer::SetMediaItem
 - mfplay/IMFPMediaPlayer::SetMediaItem
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
 - IMFPMediaPlayer.SetMediaItem
---

# IMFPMediaPlayer::SetMediaItem


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Queues a media item for playback.

## -parameters

### -param pIMFPMediaItem [in]

Pointer to the <a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem">IMFPMediaItem</a> interface of the media item.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_INVALIDARG</b></b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>MF_E_DRM_UNSUPPORTED</b></b></dt>
</dl>
</td>
<td width="60%">
The media item contains protected content. MFPlay currently does not support protected content.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>MF_E_NO_AUDIO_PLAYBACK_DEVICE</b></b></dt>
</dl>
</td>
<td width="60%">
No audio playback device was found. This error can occur if the media source contains audio, but no audio playback devices are available on the system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>MF_E_SHUTDOWN</b></b></dt>
</dl>
</td>
<td width="60%">
The object's <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-shutdown">Shutdown</a> method was called.

</td>
</tr>
</table>

## -remarks

This method completes asynchronously.  When the operation completes, the application's <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent">IMFPMediaPlayerCallback::OnMediaPlayerEvent</a> callback method is invoked. The event type is <b>MFP_EVENT_TYPE_MEDIAITEM_SET</b>.

To create a media item, call <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject">IMFPMediaPlayer::CreateMediaItemFromObject</a> or <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl">IMFPMediaPlayer::CreateMediaItemFromURL</a>. A media item must be used with the same MFPlay player object that created that item. If the media item was created by a different instance of the player object, <b>SetMediaItem</b> returns <b>E_INVALIDARG</b>.

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>