---
UID: NF:mfplay.IMFPMediaPlayer.GetBalance
title: IMFPMediaPlayer::GetBalance (mfplay.h)
description: Gets the current audio balance.
helpviewer_keywords: ["GetBalance","GetBalance method [Media Foundation]","GetBalance method [Media Foundation]","IMFPMediaPlayer interface","IMFPMediaPlayer interface [Media Foundation]","GetBalance method","IMFPMediaPlayer.GetBalance","IMFPMediaPlayer::GetBalance","mf.imfpmediaplayer_getbalance","mfplay/IMFPMediaPlayer::GetBalance"]
old-location: mf\imfpmediaplayer_getbalance.htm
tech.root: mf
ms.assetid: 27deeb41-5347-4a6d-bfd4-4e4444540651
ms.date: 12/05/2018
ms.keywords: GetBalance, GetBalance method [Media Foundation], GetBalance method [Media Foundation],IMFPMediaPlayer interface, IMFPMediaPlayer interface [Media Foundation],GetBalance method, IMFPMediaPlayer.GetBalance, IMFPMediaPlayer::GetBalance, mf.imfpmediaplayer_getbalance, mfplay/IMFPMediaPlayer::GetBalance
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
 - IMFPMediaPlayer::GetBalance
 - mfplay/IMFPMediaPlayer::GetBalance
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
 - IMFPMediaPlayer.GetBalance
---

# IMFPMediaPlayer::GetBalance


## -description

<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="/windows/desktop/medfound/media-session">Media Session</a> for playback.</div>
<div> </div>


Gets the current audio balance.

## -parameters

### -param pflBalance [out]

Receives the balance. The value can be any number in the following range (inclusive).

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>-1.0</dt>
</dl>
</td>
<td width="60%">
The left channel is at full volume; the right channel is silent.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>+1.0</dt>
</dl>
</td>
<td width="60%">
The right channel is at full volume; the left channel is silent.

</td>
</tr>
</table>
 

If the value is zero, the left and right channels are at equal volumes. The default value is zero.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>