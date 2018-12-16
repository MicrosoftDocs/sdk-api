---
UID: NF:mfplay.IMFPMediaPlayer.GetMute
title: IMFPMediaPlayer::GetMute
author: windows-sdk-content
description: Queries whether the audio is muted.
old-location: mf\imfpmediaplayer_getmute.htm
tech.root: medfound
ms.assetid: 2a628608-37ea-48f3-aed4-0344d47ede9f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetMute, GetMute method [Media Foundation], GetMute method [Media Foundation],IMFPMediaPlayer interface, IMFPMediaPlayer interface [Media Foundation],GetMute method, IMFPMediaPlayer.GetMute, IMFPMediaPlayer::GetMute, mf.imfpmediaplayer_getmute, mfplay/IMFPMediaPlayer::GetMute
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
 - IMFPMediaPlayer.GetMute
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPMediaPlayer::GetMute


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Queries whether the audio is muted.


## -parameters




### -param pfMute [out]

Receives the value <b>TRUE</b> if the audio is muted, or <b>FALSE</b> otherwise.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/fa57d465-1ee9-4f7a-9be8-66a6d73f65e8">IMFPMediaPlayer</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

