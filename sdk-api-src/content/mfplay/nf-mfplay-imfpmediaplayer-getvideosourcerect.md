---
UID: NF:mfplay.IMFPMediaPlayer.GetVideoSourceRect
title: IMFPMediaPlayer::GetVideoSourceRect (mfplay.h)
description: Gets the video source rectangle.
helpviewer_keywords: ["GetVideoSourceRect","GetVideoSourceRect method [Media Foundation]","GetVideoSourceRect method [Media Foundation]","IMFPMediaPlayer interface","IMFPMediaPlayer interface [Media Foundation]","GetVideoSourceRect method","IMFPMediaPlayer.GetVideoSourceRect","IMFPMediaPlayer::GetVideoSourceRect","mf.imfpmediaplayer_getvideosourcerect","mfplay/IMFPMediaPlayer::GetVideoSourceRect"]
old-location: mf\imfpmediaplayer_getvideosourcerect.htm
tech.root: mfarchive
archived: true
ms.assetid: 3b72ece3-f573-42e1-948c-443c793e5ba4
ms.date: 12/05/2018
ms.keywords: GetVideoSourceRect, GetVideoSourceRect method [Media Foundation], GetVideoSourceRect method [Media Foundation],IMFPMediaPlayer interface, IMFPMediaPlayer interface [Media Foundation],GetVideoSourceRect method, IMFPMediaPlayer.GetVideoSourceRect, IMFPMediaPlayer::GetVideoSourceRect, mf.imfpmediaplayer_getvideosourcerect, mfplay/IMFPMediaPlayer::GetVideoSourceRect
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
 - IMFPMediaPlayer::GetVideoSourceRect
 - mfplay/IMFPMediaPlayer::GetVideoSourceRect
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
 - IMFPMediaPlayer.GetVideoSourceRect
---

# IMFPMediaPlayer::GetVideoSourceRect


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Gets the video source rectangle.

## -parameters

### -param pnrcSource [out]

Pointer to an <a href="/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect">MFVideoNormalizedRect</a> structure that specifies the source rectangle. This rectangle defines which portion of the video is displayed. It is specified in normalized coordinates, which are defined as follows:

<ul>
<li>The upper-left corner of the video image is (0, 0).</li>
<li>The lower-right corner of  the video image is (1, 1).</li>
</ul>
If the source rectangle is {0, 0, 1, 1}, the entire image is displayed. This is the default value.

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

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>