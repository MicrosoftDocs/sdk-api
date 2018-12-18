---
UID: NF:mfplay.IMFPMediaPlayer.SetMute
title: IMFPMediaPlayer::SetMute
author: windows-sdk-content
description: Mutes or unmutes the audio.
old-location: mf\imfpmediaplayer_setmute.htm
tech.root: medfound
ms.assetid: 81e2fb76-a125-4665-9aa5-8971410ee554
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMFPMediaPlayer interface [Media Foundation],SetMute method, IMFPMediaPlayer.SetMute, IMFPMediaPlayer::SetMute, SetMute, SetMute method [Media Foundation], SetMute method [Media Foundation],IMFPMediaPlayer interface, mf.imfpmediaplayer_setmute, mfplay/IMFPMediaPlayer::SetMute
ms.topic: method
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
 - IMFPMediaPlayer.SetMute
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPMediaPlayer::SetMute


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Mutes or unmutes the audio.


## -parameters




### -param fMute

Specify <b>TRUE</b> to mute the audio, or <b>FALSE</b> to unmute the audio.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If you call this method before playback starts, the setting is applied after playback starts.

This method does not mute the entire audio session to which the player belongs. It mutes only the streams from the current media item. Other streams in the audio session are not affected. For more information, see <a href="https://msdn.microsoft.com/4cf3dd0f-4c8a-4720-9eb3-d23352f3a85e">Managing the Audio Session</a>. 





## -see-also




<a href="https://msdn.microsoft.com/fa57d465-1ee9-4f7a-9be8-66a6d73f65e8">IMFPMediaPlayer</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

