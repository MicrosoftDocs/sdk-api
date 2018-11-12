---
UID: NF:mfplay.IMFPMediaPlayer.Shutdown
title: IMFPMediaPlayer::Shutdown
author: windows-sdk-content
description: Shuts down the MFPlay player object and releases any resources the object is using.
old-location: mf\imfpmediaplayer_shutdown.htm
tech.root: medfound
ms.assetid: c56b07b5-f595-4933-9af6-868fc8938849
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: IMFPMediaPlayer interface [Media Foundation],Shutdown method, IMFPMediaPlayer.Shutdown, IMFPMediaPlayer::Shutdown, Shutdown, Shutdown method [Media Foundation], Shutdown method [Media Foundation],IMFPMediaPlayer interface, mf.imfpmediaplayer_shutdown, mfplay/IMFPMediaPlayer::Shutdown
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
 - IMFPMediaPlayer.Shutdown
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPMediaPlayer::Shutdown


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Shuts down the MFPlay player object and releases any resources the object is using.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



After this method is called, most <a href="https://msdn.microsoft.com/fa57d465-1ee9-4f7a-9be8-66a6d73f65e8">IMFPMediaPlayer</a> methods return <b>MF_E_SHUTDOWN</b>. Also, any media items created from this instance of the player object are invalidated and most <a href="https://msdn.microsoft.com/2839d256-bdaf-40cf-9f9d-46f9e2ce59e8">IMFPMediaItem</a> methods also return <b>MF_E_SHUTDOWN</b>.

The player object automatically shuts itself down when its reference count reaches zero. You can use the <b>Shutdown</b> method to shut down the player before all of the references have been released.




## -see-also




<a href="https://msdn.microsoft.com/fa57d465-1ee9-4f7a-9be8-66a6d73f65e8">IMFPMediaPlayer</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

