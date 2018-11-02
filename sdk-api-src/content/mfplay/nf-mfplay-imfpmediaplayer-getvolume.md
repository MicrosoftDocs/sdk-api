---
UID: NF:mfplay.IMFPMediaPlayer.GetVolume
title: IMFPMediaPlayer::GetVolume
author: windows-sdk-content
description: Gets the current audio volume.
old-location: mf\imfpmediaplayer_getvolume.htm
tech.root: medfound
ms.assetid: 08bf0bb3-4ee2-4229-9f41-64924c6122c9
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetVolume, GetVolume method [Media Foundation], GetVolume method [Media Foundation],IMFPMediaPlayer interface, IMFPMediaPlayer interface [Media Foundation],GetVolume method, IMFPMediaPlayer.GetVolume, IMFPMediaPlayer::GetVolume, mf.imfpmediaplayer_getvolume, mfplay/IMFPMediaPlayer::GetVolume
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
 - IMFPMediaPlayer.GetVolume
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPMediaPlayer::GetVolume


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Gets the current audio volume.


## -parameters




### -param pflVolume [out]

Receives the audio volume. Volume is expressed as an attenuation level, where 0.0 indicates silence and 1.0 indicates full volume (no attenuation).


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/fa57d465-1ee9-4f7a-9be8-66a6d73f65e8">IMFPMediaPlayer</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

