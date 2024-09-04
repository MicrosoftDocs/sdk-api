---
UID: NF:mfplay.IMFPMediaPlayer.RemoveAllEffects
title: IMFPMediaPlayer::RemoveAllEffects (mfplay.h)
description: Removes all effects that were added with the IMFPMediaPlayer::InsertEffect method.
helpviewer_keywords: ["IMFPMediaPlayer interface [Media Foundation]","RemoveAllEffects method","IMFPMediaPlayer.RemoveAllEffects","IMFPMediaPlayer::RemoveAllEffects","RemoveAllEffects","RemoveAllEffects method [Media Foundation]","RemoveAllEffects method [Media Foundation]","IMFPMediaPlayer interface","mf.imfpmediaplayer_removealleffects","mfplay/IMFPMediaPlayer::RemoveAllEffects"]
old-location: mf\imfpmediaplayer_removealleffects.htm
tech.root: mfarchive
archived: true
ms.assetid: 8745714c-315c-4183-86a2-7c189328dfe6
ms.date: 12/05/2018
ms.keywords: IMFPMediaPlayer interface [Media Foundation],RemoveAllEffects method, IMFPMediaPlayer.RemoveAllEffects, IMFPMediaPlayer::RemoveAllEffects, RemoveAllEffects, RemoveAllEffects method [Media Foundation], RemoveAllEffects method [Media Foundation],IMFPMediaPlayer interface, mf.imfpmediaplayer_removealleffects, mfplay/IMFPMediaPlayer::RemoveAllEffects
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
 - IMFPMediaPlayer::RemoveAllEffects
 - mfplay/IMFPMediaPlayer::RemoveAllEffects
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
 - IMFPMediaPlayer.RemoveAllEffects
---

# IMFPMediaPlayer::RemoveAllEffects


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Removes all effects that were added with the <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect">IMFPMediaPlayer::InsertEffect</a> method.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The change applies to the next media item that is set on the player. The effects are not removed from the current media item.

## -see-also

<a href="/windows/desktop/medfound/how-to-add-audio-or-video-effects">How to Add Audio or Video Effects</a>



<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>
