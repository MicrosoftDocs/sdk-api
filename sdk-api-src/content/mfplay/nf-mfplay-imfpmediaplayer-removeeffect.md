---
UID: NF:mfplay.IMFPMediaPlayer.RemoveEffect
title: IMFPMediaPlayer::RemoveEffect (mfplay.h)
description: Removes an effect that was added with the IMFPMediaPlayer::InsertEffect method.
helpviewer_keywords: ["IMFPMediaPlayer interface [Media Foundation]","RemoveEffect method","IMFPMediaPlayer.RemoveEffect","IMFPMediaPlayer::RemoveEffect","RemoveEffect","RemoveEffect method [Media Foundation]","RemoveEffect method [Media Foundation]","IMFPMediaPlayer interface","mf.imfpmediaplayer_removeeffect","mfplay/IMFPMediaPlayer::RemoveEffect"]
old-location: mf\imfpmediaplayer_removeeffect.htm
tech.root: mfarchive
archived: true
ms.assetid: ca8507b9-c6c5-4e17-9c18-3ec1514de897
ms.date: 12/05/2018
ms.keywords: IMFPMediaPlayer interface [Media Foundation],RemoveEffect method, IMFPMediaPlayer.RemoveEffect, IMFPMediaPlayer::RemoveEffect, RemoveEffect, RemoveEffect method [Media Foundation], RemoveEffect method [Media Foundation],IMFPMediaPlayer interface, mf.imfpmediaplayer_removeeffect, mfplay/IMFPMediaPlayer::RemoveEffect
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
 - IMFPMediaPlayer::RemoveEffect
 - mfplay/IMFPMediaPlayer::RemoveEffect
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
 - IMFPMediaPlayer.RemoveEffect
---

# IMFPMediaPlayer::RemoveEffect


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Removes an effect that was added with the <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect">IMFPMediaPlayer::InsertEffect</a> method.

## -parameters

### -param pEffect [in]

Pointer to the <b>IUnknown</b> interface of the effect object. Use the same pointer that you passed to the <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect">InsertEffect</a> method.

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
<dt><b>MF_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The effect was not found.

</td>
</tr>
</table>

## -remarks

The change applies to the next media item that is set on the player. The effect is not removed from the current media item.

## -see-also

<a href="/windows/desktop/medfound/how-to-add-audio-or-video-effects">How to Add Audio or Video Effects</a>



<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>