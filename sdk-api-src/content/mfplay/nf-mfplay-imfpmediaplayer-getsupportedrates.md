---
UID: NF:mfplay.IMFPMediaPlayer.GetSupportedRates
title: IMFPMediaPlayer::GetSupportedRates (mfplay.h)
description: Gets the range of supported playback rates.
helpviewer_keywords: ["GetSupportedRates","GetSupportedRates method [Media Foundation]","GetSupportedRates method [Media Foundation]","IMFPMediaPlayer interface","IMFPMediaPlayer interface [Media Foundation]","GetSupportedRates method","IMFPMediaPlayer.GetSupportedRates","IMFPMediaPlayer::GetSupportedRates","mf.imfpmediaplayer_getsupportedrates","mfplay/IMFPMediaPlayer::GetSupportedRates"]
old-location: mf\imfpmediaplayer_getsupportedrates.htm
tech.root: mfarchive
archived: true
ms.assetid: e0e738e4-b8e4-41da-8b74-74ce06f17274
ms.date: 12/05/2018
ms.keywords: GetSupportedRates, GetSupportedRates method [Media Foundation], GetSupportedRates method [Media Foundation],IMFPMediaPlayer interface, IMFPMediaPlayer interface [Media Foundation],GetSupportedRates method, IMFPMediaPlayer.GetSupportedRates, IMFPMediaPlayer::GetSupportedRates, mf.imfpmediaplayer_getsupportedrates, mfplay/IMFPMediaPlayer::GetSupportedRates
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
 - IMFPMediaPlayer::GetSupportedRates
 - mfplay/IMFPMediaPlayer::GetSupportedRates
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
 - IMFPMediaPlayer.GetSupportedRates
---

# IMFPMediaPlayer::GetSupportedRates


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Gets the range of supported playback rates.

## -parameters

### -param fForwardDirection [in]

Specify  <b>TRUE</b> to get the playback rates for forward playback. Specify <b>FALSE</b> to get the rates for reverse playback.

### -param pflSlowestRate [out]

Receives the slowest supported rate.

### -param pflFastestRate [out]

Receives the fastest supported rate.

## -returns

This method can return one of these values.

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
<dt><b><b>MF_E_UNSUPPORTED_RATE</b></b></dt>
</dl>
</td>
<td width="60%">
The current media item does not support playback in the requested direction (either forward or reverse).

</td>
</tr>
</table>

## -remarks

Playback rates are expressed as a ratio of the current rate to the normal rate. For example, 1.0 indicates normal playback speed, 0.5 indicates half speed, and 2.0 indicates twice speed. Positive values indicate forward playback, and negative values indicate reverse playback.

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>