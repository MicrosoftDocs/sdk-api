---
UID: NF:mfplay.IMFPMediaPlayer.GetRate
title: IMFPMediaPlayer::GetRate
author: windows-sdk-content
description: Gets the current playback rate.
old-location: mf\imfpmediaplayer_getrate.htm
tech.root: medfound
ms.assetid: 51257361-0362-43c4-8aca-81fd49be8482
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: GetRate, GetRate method [Media Foundation], GetRate method [Media Foundation],IMFPMediaPlayer interface, IMFPMediaPlayer interface [Media Foundation],GetRate method, IMFPMediaPlayer.GetRate, IMFPMediaPlayer::GetRate, mf.imfpmediaplayer_getrate, mfplay/IMFPMediaPlayer::GetRate
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
 - IMFPMediaPlayer.GetRate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPMediaPlayer::GetRate


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Gets the current playback rate.


## -parameters




### -param pflRate [out]

Receives the playback rate. The playback rate is expressed as a ratio of the current rate to the normal rate. For example, 1.0 indicates normal playback, 0.5 indicates half speed, and 2.0 indicates twice speed. Positive values indicate forward playback, and negative values indicate reverse playback.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/fa57d465-1ee9-4f7a-9be8-66a6d73f65e8">IMFPMediaPlayer</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

