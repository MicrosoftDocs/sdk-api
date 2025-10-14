---
UID: NF:mfplay.IMFPMediaPlayer.SetBalance
title: IMFPMediaPlayer::SetBalance (mfplay.h)
description: Sets the audio balance. (IMFPMediaPlayer.SetBalance)
helpviewer_keywords: ["IMFPMediaPlayer interface [Media Foundation]","SetBalance method","IMFPMediaPlayer.SetBalance","IMFPMediaPlayer::SetBalance","SetBalance","SetBalance method [Media Foundation]","SetBalance method [Media Foundation]","IMFPMediaPlayer interface","mf.imfpmediaplayer_setbalance","mfplay/IMFPMediaPlayer::SetBalance"]
old-location: mf\imfpmediaplayer_setbalance.htm
tech.root: mfarchive
archived: true
ms.assetid: cb95d037-54b4-4686-b8e6-5b960998d361
ms.date: 12/05/2018
ms.keywords: IMFPMediaPlayer interface [Media Foundation],SetBalance method, IMFPMediaPlayer.SetBalance, IMFPMediaPlayer::SetBalance, SetBalance, SetBalance method [Media Foundation], SetBalance method [Media Foundation],IMFPMediaPlayer interface, mf.imfpmediaplayer_setbalance, mfplay/IMFPMediaPlayer::SetBalance
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
 - IMFPMediaPlayer::SetBalance
 - mfplay/IMFPMediaPlayer::SetBalance
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
 - IMFPMediaPlayer.SetBalance
---

# IMFPMediaPlayer::SetBalance


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Sets the audio balance.

## -parameters

### -param flBalance [in]

The audio balance. The value can be any number in the following range (inclusive).

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>-1.0</b></dt>
</dl>
</td>
<td width="60%">
The left channel is at full volume; the right channel is silent.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>+1.0</b></dt>
</dl>
</td>
<td width="60%">
The right channel is at full volume; the left channel is silent.

</td>
</tr>
</table>
 

If the value is zero, the left and right channels are at equal volumes. The default value is zero.

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
<dt><b>MF_E_OUT_OF_RANGE</b></dt>
</dl>
</td>
<td width="60%">
The <i>flBalance</i> parameter is invalid.

</td>
</tr>
</table>

## -remarks

If you call this method before playback starts, the setting is applied when playback starts.

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>
