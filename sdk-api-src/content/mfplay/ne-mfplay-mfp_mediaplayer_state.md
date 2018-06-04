---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

