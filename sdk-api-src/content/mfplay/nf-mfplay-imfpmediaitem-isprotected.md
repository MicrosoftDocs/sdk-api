---
UID: NF:mfplay.IMFPMediaItem.IsProtected
title: IMFPMediaItem::IsProtected (mfplay.h)
description: Queries whether the media item contains protected content.
helpviewer_keywords: ["FALSE","IMFPMediaItem interface [Media Foundation]","IsProtected method","IMFPMediaItem.IsProtected","IMFPMediaItem::IsProtected","IsProtected","IsProtected method [Media Foundation]","IsProtected method [Media Foundation]","IMFPMediaItem interface","TRUE","mf.imfpmediaitem_isprotected","mfplay/IMFPMediaItem::IsProtected"]
old-location: mf\imfpmediaitem_isprotected.htm
tech.root: mfarchive
archived: true
ms.assetid: e4ae8b5e-7657-476c-83f9-c27de858e328
ms.date: 12/05/2018
ms.keywords: FALSE, IMFPMediaItem interface [Media Foundation],IsProtected method, IMFPMediaItem.IsProtected, IMFPMediaItem::IsProtected, IsProtected, IsProtected method [Media Foundation], IsProtected method [Media Foundation],IMFPMediaItem interface, TRUE, mf.imfpmediaitem_isprotected, mfplay/IMFPMediaItem::IsProtected
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
 - IMFPMediaItem::IsProtected
 - mfplay/IMFPMediaItem::IsProtected
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
 - IMFPMediaItem.IsProtected
---

# IMFPMediaItem::IsProtected


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Queries whether the media item contains protected content.
<div class="alert"><b>Note</b>  Currently <a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a> does not support playing protected content.</div><div> </div>

## -parameters

### -param pfProtected [out]

Receives one of the following values.

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
The media item contains protected content. Attempting to play this media item will cause a playback error.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The media item does not contain protected content.

</td>
</tr>
</table>

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem">IMFPMediaItem</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>