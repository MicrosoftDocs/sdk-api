---
UID: NF:mfplay.IMFPMediaItem.GetMediaPlayer
title: IMFPMediaItem::GetMediaPlayer method
author: windows-driver-content
description: Gets a pointer to the MFPlay player object that created the media item.
old-location: mf\imfpmediaitem_getmediaplayer.htm
old-project: medfound
ms.assetid: 6d6f822a-d599-437e-a73a-2242d4d3fe3a
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: GetMediaPlayer method [Media Foundation], GetMediaPlayer method [Media Foundation], IMFPMediaItem interface, GetMediaPlayer,IMFPMediaItem.GetMediaPlayer, IMFPMediaItem, IMFPMediaItem interface [Media Foundation], GetMediaPlayer method, IMFPMediaItem::GetMediaPlayer, mf.imfpmediaitem_getmediaplayer, mfplay/IMFPMediaItem::GetMediaPlayer
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
-	IMFPMediaItem.GetMediaPlayer
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFPMediaItem::GetMediaPlayer method


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Gets a pointer to the MFPlay player object that created the media item.


## -parameters




### -param ppMediaPlayer [out]

Receives a pointer to the player object's <a href="https://msdn.microsoft.com/fa57d465-1ee9-4f7a-9be8-66a6d73f65e8">IMFPMediaPlayer</a> interface. The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2839d256-bdaf-40cf-9f9d-46f9e2ce59e8">IMFPMediaItem</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

