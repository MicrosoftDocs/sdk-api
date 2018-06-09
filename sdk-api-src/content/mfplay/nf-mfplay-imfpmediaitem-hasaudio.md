---
UID: NF:mfplay.IMFPMediaItem.HasAudio
title: IMFPMediaItem::HasAudio
author: windows-sdk-content
description: Queries whether the media item contains an audio stream.
old-location: mf\imfpmediaitem_hasaudio.htm
old-project: medfound
ms.assetid: 38d308d7-77e3-4f13-82e7-677ac94234e7
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: HasAudio, HasAudio method [Media Foundation], HasAudio method [Media Foundation],IMFPMediaItem interface, IMFPMediaItem interface [Media Foundation],HasAudio method, IMFPMediaItem.HasAudio, IMFPMediaItem::HasAudio, mf.imfpmediaitem_hasaudio, mfplay/IMFPMediaItem::HasAudio
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: "_MFP_MEDIAITEM_CHARACTERISTICS"
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplay.h
api_name:
 - IMFPMediaItem.HasAudio
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFPMediaItem::HasAudio


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Queries whether the media item contains an audio stream.


## -parameters




### -param pfHasAudio [out]

Receives the value <b>TRUE</b> if the media item contains at least one audio stream, or <b>FALSE</b> otherwise.


### -param pfSelected [out]

Receives the value <b>TRUE</b> if at least one audio stream is selected, or <b>FALSE</b> otherwise.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




        To select or deselect streams before playback starts, call <a href="https://msdn.microsoft.com/739190a5-60a7-4b50-9919-f68d2cd6da8d">IMFPMediaItem::SetStreamSelection</a>.




## -see-also




<a href="https://msdn.microsoft.com/2839d256-bdaf-40cf-9f9d-46f9e2ce59e8">IMFPMediaItem</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

