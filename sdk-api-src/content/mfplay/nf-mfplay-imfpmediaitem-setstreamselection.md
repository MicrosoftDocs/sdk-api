---
UID: NF:mfplay.IMFPMediaItem.SetStreamSelection
title: IMFPMediaItem::SetStreamSelection (mfplay.h)
description: Selects or deselects a stream.
helpviewer_keywords: ["FALSE","IMFPMediaItem interface [Media Foundation]","SetStreamSelection method","IMFPMediaItem.SetStreamSelection","IMFPMediaItem::SetStreamSelection","SetStreamSelection","SetStreamSelection method [Media Foundation]","SetStreamSelection method [Media Foundation]","IMFPMediaItem interface","TRUE","mf.imfpmediaitem_setstreamselection","mfplay/IMFPMediaItem::SetStreamSelection"]
old-location: mf\imfpmediaitem_setstreamselection.htm
tech.root: mf
ms.assetid: 739190a5-60a7-4b50-9919-f68d2cd6da8d
ms.date: 12/05/2018
ms.keywords: FALSE, IMFPMediaItem interface [Media Foundation],SetStreamSelection method, IMFPMediaItem.SetStreamSelection, IMFPMediaItem::SetStreamSelection, SetStreamSelection, SetStreamSelection method [Media Foundation], SetStreamSelection method [Media Foundation],IMFPMediaItem interface, TRUE, mf.imfpmediaitem_setstreamselection, mfplay/IMFPMediaItem::SetStreamSelection
f1_keywords:
- mfplay/IMFPMediaItem.SetStreamSelection
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfplay.h
api_name:
- IMFPMediaItem.SetStreamSelection
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFPMediaItem::SetStreamSelection


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://docs.microsoft.com/windows/desktop/medfound/media-session">Media Session</a> for playback.</div>
<div> </div>


Selects or deselects a stream.


## -parameters




### -param dwStreamIndex [in]

Zero-based index of the stream. To get the number of streams, call <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getnumberofstreams">IMFPMediaItem::GetNumberOfStreams</a>.


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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You can use this method to change which streams are selected. The change goes into effect the next time that <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem">IMFPMediaPlayer::SetMediaItem</a> is called with this media item. If the media item is already set on the player, the change does not happen unless you call <b>SetMediaItem</b> again with this media item.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem">IMFPMediaItem</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>
 

 

