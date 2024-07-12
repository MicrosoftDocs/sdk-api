---
UID: NF:mfplay.IMFPMediaPlayer.SetVolume
title: IMFPMediaPlayer::SetVolume (mfplay.h)
description: Sets the audio volume.
helpviewer_keywords: ["IMFPMediaPlayer interface [Media Foundation]","SetVolume method","IMFPMediaPlayer.SetVolume","IMFPMediaPlayer::SetVolume","SetVolume","SetVolume method [Media Foundation]","SetVolume method [Media Foundation]","IMFPMediaPlayer interface","mf.imfpmediaplayer_setvolume","mfplay/IMFPMediaPlayer::SetVolume"]
old-location: mf\imfpmediaplayer_setvolume.htm
tech.root: mfarchive
archived: true
ms.assetid: feee2812-7c7e-4c27-86be-8f7316854222
ms.date: 12/05/2018
ms.keywords: IMFPMediaPlayer interface [Media Foundation],SetVolume method, IMFPMediaPlayer.SetVolume, IMFPMediaPlayer::SetVolume, SetVolume, SetVolume method [Media Foundation], SetVolume method [Media Foundation],IMFPMediaPlayer interface, mf.imfpmediaplayer_setvolume, mfplay/IMFPMediaPlayer::SetVolume
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
 - IMFPMediaPlayer::SetVolume
 - mfplay/IMFPMediaPlayer::SetVolume
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
 - IMFPMediaPlayer.SetVolume
---

# IMFPMediaPlayer::SetVolume


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Sets the audio volume.

## -parameters

### -param flVolume [in]

The volume level. Volume is expressed as an attenuation level, where 0.0 indicates silence and 1.0 indicates full volume (no attenuation).

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
The <i>flVolume</i> parameter is invalid.

</td>
</tr>
</table>

## -remarks

If you call this method before playback starts, the setting is applied after playback starts.

This method does not change the master volume level for the player's audio session. Instead, it adjusts the per-channel volume levels for audio stream(s) that belong to the current media item. Other streams in the audio session are not affected. For more information, see <a href="/windows/desktop/medfound/managing-the-audio-session">Managing the Audio Session</a>.

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>