---
UID: NF:mfplay.IMFPMediaPlayer.GetVolume
title: IMFPMediaPlayer::GetVolume (mfplay.h)
description: Gets the current audio volume.
helpviewer_keywords: ["GetVolume","GetVolume method [Media Foundation]","GetVolume method [Media Foundation]","IMFPMediaPlayer interface","IMFPMediaPlayer interface [Media Foundation]","GetVolume method","IMFPMediaPlayer.GetVolume","IMFPMediaPlayer::GetVolume","mf.imfpmediaplayer_getvolume","mfplay/IMFPMediaPlayer::GetVolume"]
old-location: mf\imfpmediaplayer_getvolume.htm
tech.root: mf
ms.assetid: 08bf0bb3-4ee2-4229-9f41-64924c6122c9
ms.date: 12/05/2018
ms.keywords: GetVolume, GetVolume method [Media Foundation], GetVolume method [Media Foundation],IMFPMediaPlayer interface, IMFPMediaPlayer interface [Media Foundation],GetVolume method, IMFPMediaPlayer.GetVolume, IMFPMediaPlayer::GetVolume, mf.imfpmediaplayer_getvolume, mfplay/IMFPMediaPlayer::GetVolume
f1_keywords:
- mfplay/IMFPMediaPlayer.GetVolume
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
- IMFPMediaPlayer.GetVolume
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFPMediaPlayer::GetVolume


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://docs.microsoft.com/windows/desktop/medfound/media-session">Media Session</a> for playback.</div>
<div> </div>


Gets the current audio volume.


## -parameters




### -param pflVolume [out]

Receives the audio volume. Volume is expressed as an attenuation level, where 0.0 indicates silence and 1.0 indicates full volume (no attenuation).


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>
 

 

