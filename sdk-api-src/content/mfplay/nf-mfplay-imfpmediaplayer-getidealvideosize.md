---
UID: NF:mfplay.IMFPMediaPlayer.GetIdealVideoSize
title: IMFPMediaPlayer::GetIdealVideoSize (mfplay.h)
description: Gets the range of video sizes that can be displayed without significantly degrading performance or image quality.
helpviewer_keywords: ["GetIdealVideoSize","GetIdealVideoSize method [Media Foundation]","GetIdealVideoSize method [Media Foundation]","IMFPMediaPlayer interface","IMFPMediaPlayer interface [Media Foundation]","GetIdealVideoSize method","IMFPMediaPlayer.GetIdealVideoSize","IMFPMediaPlayer::GetIdealVideoSize","mf.imfpmediaplayer_getidealvideosize","mfplay/IMFPMediaPlayer::GetIdealVideoSize"]
old-location: mf\imfpmediaplayer_getidealvideosize.htm
tech.root: mfarchive
archived: true
ms.assetid: e6835852-10f0-4453-a22a-a567457bd7c5
ms.date: 12/05/2018
ms.keywords: GetIdealVideoSize, GetIdealVideoSize method [Media Foundation], GetIdealVideoSize method [Media Foundation],IMFPMediaPlayer interface, IMFPMediaPlayer interface [Media Foundation],GetIdealVideoSize method, IMFPMediaPlayer.GetIdealVideoSize, IMFPMediaPlayer::GetIdealVideoSize, mf.imfpmediaplayer_getidealvideosize, mfplay/IMFPMediaPlayer::GetIdealVideoSize
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
 - IMFPMediaPlayer::GetIdealVideoSize
 - mfplay/IMFPMediaPlayer::GetIdealVideoSize
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
 - IMFPMediaPlayer.GetIdealVideoSize
---

# IMFPMediaPlayer::GetIdealVideoSize


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Gets the range of video sizes that can be displayed without significantly degrading performance or image quality.

## -parameters

### -param pszMin [out]

Receives the minimum size that is preferable. This parameter can be <b>NULL</b>.

### -param pszMax [out]

Receives the maximum size that is preferable. This parameter can be <b>NULL</b>.

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
<dt><b><b>MF_E_INVALIDREQUEST</b></b></dt>
</dl>
</td>
<td width="60%">
The current media item does not contain video.

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

At least one parameter must be non-<b>NULL</b>. Sizes are given in pixels.

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>