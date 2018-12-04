---
UID: NF:mfplay.IMFPMediaPlayer.RemoveAllEffects
title: IMFPMediaPlayer::RemoveAllEffects
author: windows-sdk-content
description: Removes all effects that were added with the IMFPMediaPlayer::InsertEffect method.
old-location: mf\imfpmediaplayer_removealleffects.htm
tech.root: medfound
ms.assetid: 8745714c-315c-4183-86a2-7c189328dfe6
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: IMFPMediaPlayer interface [Media Foundation],RemoveAllEffects method, IMFPMediaPlayer.RemoveAllEffects, IMFPMediaPlayer::RemoveAllEffects, RemoveAllEffects, RemoveAllEffects method [Media Foundation], RemoveAllEffects method [Media Foundation],IMFPMediaPlayer interface, mf.imfpmediaplayer_removealleffects, mfplay/IMFPMediaPlayer::RemoveAllEffects
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IMFPMediaPlayer.RemoveAllEffects
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPMediaPlayer::RemoveAllEffects


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Removes all effects that were added with the <a href="https://msdn.microsoft.com/2689ee46-5cfe-4616-850c-eb5aef340daa">IMFPMediaPlayer::InsertEffect</a> method.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The change applies to the next media item that is set on the player. The effects are not removed from the current media item.




## -see-also




<a href="https://msdn.microsoft.com/90f34bf3-899f-46e0-80c8-af83caa4835d">How to Add Audio or Video Effects</a>



<a href="https://msdn.microsoft.com/fa57d465-1ee9-4f7a-9be8-66a6d73f65e8">IMFPMediaPlayer</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

