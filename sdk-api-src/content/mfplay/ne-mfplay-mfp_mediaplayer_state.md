---
UID: NE:mfplay.MFP_MEDIAPLAYER_STATE
title: MFP_MEDIAPLAYER_STATE
author: windows-sdk-content
description: Specifies the current playback state.
old-location: mf\mfp_mediaplayer_state.htm
tech.root: medfound
ms.assetid: a0d5c840-a1aa-48cf-bf2e-7e5c35951fb6
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: MFP_MEDIAPLAYER_STATE, MFP_MEDIAPLAYER_STATE enumeration [Media Foundation], MFP_MEDIAPLAYER_STATE_EMPTY, MFP_MEDIAPLAYER_STATE_PAUSED, MFP_MEDIAPLAYER_STATE_PLAYING, MFP_MEDIAPLAYER_STATE_SHUTDOWN, MFP_MEDIAPLAYER_STATE_STOPPED, mf.mfp_mediaplayer_state, mfplay/MFP_MEDIAPLAYER_STATE, mfplay/MFP_MEDIAPLAYER_STATE_EMPTY, mfplay/MFP_MEDIAPLAYER_STATE_PAUSED, mfplay/MFP_MEDIAPLAYER_STATE_PLAYING, mfplay/MFP_MEDIAPLAYER_STATE_SHUTDOWN, mfplay/MFP_MEDIAPLAYER_STATE_STOPPED
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfplay.h
api_name:
 - MFP_MEDIAPLAYER_STATE
product: Windows
targetos: Windows
req.typenames: MFP_MEDIAPLAYER_STATE
req.redist: 
---

# MFP_MEDIAPLAYER_STATE enumeration


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Specifies the current playback state.


## -enum-fields




### -field MFP_MEDIAPLAYER_STATE_EMPTY

Initial state. No media items have been set on the player object.


### -field MFP_MEDIAPLAYER_STATE_STOPPED

Playback is stopped.


### -field MFP_MEDIAPLAYER_STATE_PLAYING

Playback is in progress.


### -field MFP_MEDIAPLAYER_STATE_PAUSED

Playback is paused.


### -field MFP_MEDIAPLAYER_STATE_SHUTDOWN

The player object was shut down. This state is returned after the application calls <a href="https://msdn.microsoft.com/c56b07b5-f595-4933-9af6-868fc8938849">IMFPMediaPlayer::Shutdown</a>.


## -see-also




<a href="https://msdn.microsoft.com/072c5e93-b3ce-469c-8235-3e9c63bd77e3">IMFPMediaPlayer::GetState</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

