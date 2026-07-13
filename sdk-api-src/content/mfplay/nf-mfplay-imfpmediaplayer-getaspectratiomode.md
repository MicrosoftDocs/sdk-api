---
UID: NF:mfplay.IMFPMediaPlayer.GetAspectRatioMode
title: IMFPMediaPlayer::GetAspectRatioMode (mfplay.h)
description: Gets the current aspect-ratio correction mode. This mode controls whether the aspect ratio of the video is preserved during playback.
helpviewer_keywords: ["GetAspectRatioMode","GetAspectRatioMode method [Media Foundation]","GetAspectRatioMode method [Media Foundation]","IMFPMediaPlayer interface","IMFPMediaPlayer interface [Media Foundation]","GetAspectRatioMode method","IMFPMediaPlayer.GetAspectRatioMode","IMFPMediaPlayer::GetAspectRatioMode","mf.imfpmediaplayer_getaspectratiomode","mfplay/IMFPMediaPlayer::GetAspectRatioMode"]
old-location: mf\imfpmediaplayer_getaspectratiomode.htm
tech.root: mfarchive
archived: true
ms.assetid: eaeb20d2-d547-4f88-a69f-7c3f46fe95ff
ms.date: 12/05/2018
ms.keywords: GetAspectRatioMode, GetAspectRatioMode method [Media Foundation], GetAspectRatioMode method [Media Foundation],IMFPMediaPlayer interface, IMFPMediaPlayer interface [Media Foundation],GetAspectRatioMode method, IMFPMediaPlayer.GetAspectRatioMode, IMFPMediaPlayer::GetAspectRatioMode, mf.imfpmediaplayer_getaspectratiomode, mfplay/IMFPMediaPlayer::GetAspectRatioMode
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
 - IMFPMediaPlayer::GetAspectRatioMode
 - mfplay/IMFPMediaPlayer::GetAspectRatioMode
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
 - IMFPMediaPlayer.GetAspectRatioMode
---

# IMFPMediaPlayer::GetAspectRatioMode


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Gets the current aspect-ratio correction mode. This mode controls whether the aspect ratio of the video is preserved during playback.

## -parameters

### -param pdwAspectRatioMode [out]

Receives a bitwise <b>OR</b> of one or more flags from the <a href="/windows/desktop/api/evr/ne-evr-mfvideoaspectratiomode">MFVideoAspectRatioMode</a> enumeration.

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
<dt><b>S_OK</b></dt>
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

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>