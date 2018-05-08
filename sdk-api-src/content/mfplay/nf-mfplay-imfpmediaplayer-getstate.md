---
UID: NF:mfplay.IMFPMediaPlayer.GetState
title: IMFPMediaPlayer::GetState
author: windows-driver-content
description: Gets the current playback state of the MFPlay player object.
old-location: mf\imfpmediaplayer_getstate.htm
old-project: medfound
ms.assetid: 072c5e93-b3ce-469c-8235-3e9c63bd77e3
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: GetState, GetState method [Media Foundation], GetState method [Media Foundation],IMFPMediaPlayer interface, IMFPMediaPlayer interface [Media Foundation],GetState method, IMFPMediaPlayer.GetState, IMFPMediaPlayer::GetState, mf.imfpmediaplayer_getstate, mfplay/IMFPMediaPlayer::GetState
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
req.typenames: "_MFP_MEDIAITEM_CHARACTERISTICS"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfplay.h
api_name:
-	IMFPMediaPlayer.GetState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFPMediaPlayer::GetState


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Gets the current playback state of the MFPlay player object.


## -parameters




### -param peState [out]

Receives the playback state, as a member of the <a href="https://msdn.microsoft.com/a0d5c840-a1aa-48cf-bf2e-7e5c35951fb6">MFP_MEDIAPLAYER_STATE</a> enumeration.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method can be called after the player object has been shut down.

Many of the <a href="https://msdn.microsoft.com/fa57d465-1ee9-4f7a-9be8-66a6d73f65e8">IMFPMediaPlayer</a> methods complete asynchronously. While an asynchronous operation is pending, the current state is not updated until the operation completes. When the operation completes, the application receives an event callback, and the new state is given in the <a href="https://msdn.microsoft.com/ed9d3790-845a-4392-b755-6a5ce6e20de5">MFP_EVENT_HEADER</a> structure that is passed to the callback.




## -see-also




<a href="https://msdn.microsoft.com/fa57d465-1ee9-4f7a-9be8-66a6d73f65e8">IMFPMediaPlayer</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

