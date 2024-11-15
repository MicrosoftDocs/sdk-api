---
UID: NF:mfplay.IMFPMediaPlayer.SetVideoSourceRect
title: IMFPMediaPlayer::SetVideoSourceRect (mfplay.h)
description: Sets the video source rectangle.
helpviewer_keywords: ["IMFPMediaPlayer interface [Media Foundation]","SetVideoSourceRect method","IMFPMediaPlayer.SetVideoSourceRect","IMFPMediaPlayer::SetVideoSourceRect","SetVideoSourceRect","SetVideoSourceRect method [Media Foundation]","SetVideoSourceRect method [Media Foundation]","IMFPMediaPlayer interface","mf.imfpmediaplayer_setvideosourcerect","mfplay/IMFPMediaPlayer::SetVideoSourceRect"]
old-location: mf\imfpmediaplayer_setvideosourcerect.htm
tech.root: mfarchive
archived: true
ms.assetid: c95d724f-40a9-43c5-b81a-8505eda516f7
ms.date: 12/05/2018
ms.keywords: IMFPMediaPlayer interface [Media Foundation],SetVideoSourceRect method, IMFPMediaPlayer.SetVideoSourceRect, IMFPMediaPlayer::SetVideoSourceRect, SetVideoSourceRect, SetVideoSourceRect method [Media Foundation], SetVideoSourceRect method [Media Foundation],IMFPMediaPlayer interface, mf.imfpmediaplayer_setvideosourcerect, mfplay/IMFPMediaPlayer::SetVideoSourceRect
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
 - IMFPMediaPlayer::SetVideoSourceRect
 - mfplay/IMFPMediaPlayer::SetVideoSourceRect
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
 - IMFPMediaPlayer.SetVideoSourceRect
---

# IMFPMediaPlayer::SetVideoSourceRect


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Sets the video source rectangle.

MFPlay clips the video to this rectangle and stretches the rectangle to fill the video window.

## -parameters

### -param pnrcSource [in]

Pointer to an <a href="/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect">MFVideoNormalizedRect</a> structure that specifies the source rectangle. This rectangle defines which portion of the video is displayed. It is specified in normalized coordinates, which are defined as follows:

<ul>
<li>The upper-left corner of the video image is (0, 0).</li>
<li>The lower-right corner of  the video image is (1, 1).</li>
</ul>
To display the entire image, set the source rectangle to {0, 0, 1, 1}. This is the default value.

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

## -remarks

MFPlay stretches the source rectangle to fill the entire video window. By default, MFPlay maintains the source's correct aspect ratio, letterboxing if needed. The letterbox color is controlled by the <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setbordercolor">IMFPMediaPlayer::SetBorderColor</a> method.

This method fails if no media item is currently set, or if the current media item does not contain video.

To set the video position before playback starts, call this method inside your event handler for the <b>MFP_EVENT_TYPE_MEDIAITEM_SET</b> event. For more information, see <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent">IMFPMediaPlayerCallback::OnMediaPlayerEvent</a>.

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>