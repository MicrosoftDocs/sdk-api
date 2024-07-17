---
UID: NF:mfplay.IMFPMediaItem.SetStreamSelection
title: IMFPMediaItem::SetStreamSelection (mfplay.h)
description: Selects or deselects a stream.
helpviewer_keywords: ["FALSE","IMFPMediaItem interface [Media Foundation]","SetStreamSelection method","IMFPMediaItem.SetStreamSelection","IMFPMediaItem::SetStreamSelection","SetStreamSelection","SetStreamSelection method [Media Foundation]","SetStreamSelection method [Media Foundation]","IMFPMediaItem interface","TRUE","mf.imfpmediaitem_setstreamselection","mfplay/IMFPMediaItem::SetStreamSelection"]
old-location: mf\imfpmediaitem_setstreamselection.htm
tech.root: mfarchive
archived: true
ms.assetid: 739190a5-60a7-4b50-9919-f68d2cd6da8d
ms.date: 12/05/2018
ms.keywords: FALSE, IMFPMediaItem interface [Media Foundation],SetStreamSelection method, IMFPMediaItem.SetStreamSelection, IMFPMediaItem::SetStreamSelection, SetStreamSelection, SetStreamSelection method [Media Foundation], SetStreamSelection method [Media Foundation],IMFPMediaItem interface, TRUE, mf.imfpmediaitem_setstreamselection, mfplay/IMFPMediaItem::SetStreamSelection
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
 - IMFPMediaItem::SetStreamSelection
 - mfplay/IMFPMediaItem::SetStreamSelection
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
 - IMFPMediaItem.SetStreamSelection
---

# IMFPMediaItem::SetStreamSelection


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Selects or deselects a stream.

## -parameters

### -param dwStreamIndex [in]

Zero-based index of the stream. To get the number of streams, call <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getnumberofstreams">IMFPMediaItem::GetNumberOfStreams</a>.

### -param fEnabled [in]

Specify whether to select or deselect the stream.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The stream is selected. During playback, this stream will play.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The stream is not selected. During playback, this stream will not play.

</td>
</tr>
</table>

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

You can use this method to change which streams are selected. The change goes into effect the next time that <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem">IMFPMediaPlayer::SetMediaItem</a> is called with this media item. If the media item is already set on the player, the change does not happen unless you call <b>SetMediaItem</b> again with this media item.

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem">IMFPMediaItem</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>