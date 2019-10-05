---
UID: NF:mfplay.IMFPMediaPlayer.RemoveAllEffects
title: IMFPMediaPlayer::RemoveAllEffects (mfplay.h)
author: windows-sdk-content
description: Removes all effects that were added with the IMFPMediaPlayer::InsertEffect method.
old-location: mf\imfpmediaplayer_removealleffects.htm
tech.root: medfound
ms.assetid: 8745714c-315c-4183-86a2-7c189328dfe6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFPMediaPlayer interface [Media Foundation],RemoveAllEffects method, IMFPMediaPlayer.RemoveAllEffects, IMFPMediaPlayer::RemoveAllEffects, RemoveAllEffects, RemoveAllEffects method [Media Foundation], RemoveAllEffects method [Media Foundation],IMFPMediaPlayer interface, mf.imfpmediaplayer_removealleffects, mfplay/IMFPMediaPlayer::RemoveAllEffects
ms.topic: method
f1_keywords: 
 - "mfplay/IMFPMediaPlayer.RemoveAllEffects"
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
 - IMFPMediaPlayer.RemoveAllEffects
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFPMediaPlayer::RemoveAllEffects


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://docs.microsoft.com/windows/desktop/medfound/media-session">Media Session</a> for playback.</div>
<div> </div>


Removes all effects that were added with the <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect">IMFPMediaPlayer::InsertEffect</a> method.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The change applies to the next media item that is set on the player. The effects are not removed from the current media item.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/how-to-add-audio-or-video-effects">How to Add Audio or Video Effects</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>
 

 

