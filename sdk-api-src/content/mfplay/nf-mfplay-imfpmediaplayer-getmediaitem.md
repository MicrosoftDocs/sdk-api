---
UID: NF:mfplay.IMFPMediaPlayer.GetMediaItem
title: IMFPMediaPlayer::GetMediaItem (mfplay.h)
description: Gets a pointer to the current media item.
helpviewer_keywords: ["GetMediaItem","GetMediaItem method [Media Foundation]","GetMediaItem method [Media Foundation]","IMFPMediaPlayer interface","IMFPMediaPlayer interface [Media Foundation]","GetMediaItem method","IMFPMediaPlayer.GetMediaItem","IMFPMediaPlayer::GetMediaItem","mf.imfpmediaplayer_getmediaitem","mfplay/IMFPMediaPlayer::GetMediaItem"]
old-location: mf\imfpmediaplayer_getmediaitem.htm
tech.root: mfarchive
archived: true
ms.assetid: 9593092d-bd50-4ff6-a283-f5a0ab1e6fc0
ms.date: 12/05/2018
ms.keywords: GetMediaItem, GetMediaItem method [Media Foundation], GetMediaItem method [Media Foundation],IMFPMediaPlayer interface, IMFPMediaPlayer interface [Media Foundation],GetMediaItem method, IMFPMediaPlayer.GetMediaItem, IMFPMediaPlayer::GetMediaItem, mf.imfpmediaplayer_getmediaitem, mfplay/IMFPMediaPlayer::GetMediaItem
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
 - IMFPMediaPlayer::GetMediaItem
 - mfplay/IMFPMediaPlayer::GetMediaItem
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
 - IMFPMediaPlayer.GetMediaItem
---

# IMFPMediaPlayer::GetMediaItem


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Gets a pointer to the current media item.

## -parameters

### -param ppIMFPMediaItem [out]

Receives a pointer to the media item's <a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem">IMFPMediaItem</a> interface. The caller must release the interface.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
There is no current media item.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
There is no current media item.

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

The <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem">IMFPMediaPlayer::SetMediaItem</a> method is asynchronous. Therefore, while <b>SetMediaItem</b> is pending, <b>GetMediaItem</b> will not return the media item that was just set. Instead, the application should implement <a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback">IMFPMediaPlayerCallback</a> interface and handle the <b>MFP_EVENT_TYPE_MEDIAITEM_SET</b> event. For more information, see <a href="/windows/desktop/medfound/getting-started-with-mfplay">Receiving Events From the Player</a>.

The previous remark also applies to setting the media item in the <a href="/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer">MFPCreateMediaPlayer</a> function.

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>