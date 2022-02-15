---
UID: NE:mfplay.MFP_MEDIAPLAYER_STATE
title: MFP_MEDIAPLAYER_STATE (mfplay.h)
description: Specifies the current playback state.
helpviewer_keywords: ["MFP_MEDIAPLAYER_STATE","MFP_MEDIAPLAYER_STATE enumeration [Media Foundation]","MFP_MEDIAPLAYER_STATE_EMPTY","MFP_MEDIAPLAYER_STATE_PAUSED","MFP_MEDIAPLAYER_STATE_PLAYING","MFP_MEDIAPLAYER_STATE_SHUTDOWN","MFP_MEDIAPLAYER_STATE_STOPPED","mf.mfp_mediaplayer_state","mfplay/MFP_MEDIAPLAYER_STATE","mfplay/MFP_MEDIAPLAYER_STATE_EMPTY","mfplay/MFP_MEDIAPLAYER_STATE_PAUSED","mfplay/MFP_MEDIAPLAYER_STATE_PLAYING","mfplay/MFP_MEDIAPLAYER_STATE_SHUTDOWN","mfplay/MFP_MEDIAPLAYER_STATE_STOPPED"]
old-location: mf\mfp_mediaplayer_state.htm
tech.root: mf
ms.assetid: a0d5c840-a1aa-48cf-bf2e-7e5c35951fb6
ms.date: 12/05/2018
ms.keywords: MFP_MEDIAPLAYER_STATE, MFP_MEDIAPLAYER_STATE enumeration [Media Foundation], MFP_MEDIAPLAYER_STATE_EMPTY, MFP_MEDIAPLAYER_STATE_PAUSED, MFP_MEDIAPLAYER_STATE_PLAYING, MFP_MEDIAPLAYER_STATE_SHUTDOWN, MFP_MEDIAPLAYER_STATE_STOPPED, mf.mfp_mediaplayer_state, mfplay/MFP_MEDIAPLAYER_STATE, mfplay/MFP_MEDIAPLAYER_STATE_EMPTY, mfplay/MFP_MEDIAPLAYER_STATE_PAUSED, mfplay/MFP_MEDIAPLAYER_STATE_PLAYING, mfplay/MFP_MEDIAPLAYER_STATE_SHUTDOWN, mfplay/MFP_MEDIAPLAYER_STATE_STOPPED
req.header: mfplay.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfplay.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MFP_MEDIAPLAYER_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFP_MEDIAPLAYER_STATE
 - mfplay/MFP_MEDIAPLAYER_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfplay.h
api_name:
 - MFP_MEDIAPLAYER_STATE
---

# MFP_MEDIAPLAYER_STATE enumeration


## -description

<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="/windows/desktop/medfound/media-session">Media Session</a> for playback.</div>
<div> </div>


Specifies the current playback state.

## -enum-fields

### -field MFP_MEDIAPLAYER_STATE_EMPTY:0

Initial state. No media items have been set on the player object.

### -field MFP_MEDIAPLAYER_STATE_STOPPED:0x1

Playback is stopped.

### -field MFP_MEDIAPLAYER_STATE_PLAYING:0x2

Playback is in progress.

### -field MFP_MEDIAPLAYER_STATE_PAUSED:0x3

Playback is paused.

### -field MFP_MEDIAPLAYER_STATE_SHUTDOWN:0x4

The player object was shut down. This state is returned after the application calls <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-shutdown">IMFPMediaPlayer::Shutdown</a>.

## -see-also

<a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getstate">IMFPMediaPlayer::GetState</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
