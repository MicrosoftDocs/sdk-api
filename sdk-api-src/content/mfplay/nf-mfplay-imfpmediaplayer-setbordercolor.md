---
UID: NF:mfplay.IMFPMediaPlayer.SetBorderColor
title: IMFPMediaPlayer::SetBorderColor (mfplay.h)
description: Sets the color for the video border.
helpviewer_keywords: ["IMFPMediaPlayer interface [Media Foundation]","SetBorderColor method","IMFPMediaPlayer.SetBorderColor","IMFPMediaPlayer::SetBorderColor","SetBorderColor","SetBorderColor method [Media Foundation]","SetBorderColor method [Media Foundation]","IMFPMediaPlayer interface","mf.imfpmediaplayer_setbordercolor","mfplay/IMFPMediaPlayer::SetBorderColor"]
old-location: mf\imfpmediaplayer_setbordercolor.htm
tech.root: mfarchive
archived: true
ms.assetid: f66b671d-0c7d-4261-8210-05f2d2f8d9a5
ms.date: 12/05/2018
ms.keywords: IMFPMediaPlayer interface [Media Foundation],SetBorderColor method, IMFPMediaPlayer.SetBorderColor, IMFPMediaPlayer::SetBorderColor, SetBorderColor, SetBorderColor method [Media Foundation], SetBorderColor method [Media Foundation],IMFPMediaPlayer interface, mf.imfpmediaplayer_setbordercolor, mfplay/IMFPMediaPlayer::SetBorderColor
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
 - IMFPMediaPlayer::SetBorderColor
 - mfplay/IMFPMediaPlayer::SetBorderColor
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
 - IMFPMediaPlayer.SetBorderColor
---

# IMFPMediaPlayer::SetBorderColor


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Sets the color for the video border. The border color is used to letterbox the video.

## -parameters

### -param Clr [in]

Specifies the border color as a <b>COLORREF</b> value. Use the <b>RGB</b> macro to create this value. The default value is black.

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
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
The current media item does not contain video.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The object's <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-shutdown">Shutdown</a> method was called.

</td>
</tr>
</table>

## -remarks

This method fails if no media item is currently set, or if the current media item does not contain video.

To set the border color before playback starts, call this method inside your event handler for the <b>MFP_EVENT_TYPE_MEDIAITEM_SET</b> event. For more information, see <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent">IMFPMediaPlayerCallback::OnMediaPlayerEvent</a>.

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>