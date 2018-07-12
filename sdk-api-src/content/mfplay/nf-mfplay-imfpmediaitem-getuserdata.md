---
UID: NF:mfplay.IMFPMediaItem.GetUserData
title: IMFPMediaItem::GetUserData
author: windows-sdk-content
description: Gets the application-defined value stored in the media item.
old-location: mf\imfpmediaitem_getuserdata.htm
old-project: medfound
ms.assetid: aa99ced1-c32b-4bf5-b29a-e16eceddfed1
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetUserData, GetUserData method [Media Foundation], GetUserData method [Media Foundation],IMFPMediaItem interface, IMFPMediaItem interface [Media Foundation],GetUserData method, IMFPMediaItem.GetUserData, IMFPMediaItem::GetUserData, mf.imfpmediaitem_getuserdata, mfplay/IMFPMediaItem::GetUserData
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
 - IMFPMediaItem.GetUserData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFPMediaItem::GetUserData


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Gets the application-defined value stored in the media item.


## -parameters




### -param pdwUserData [out]

Receives the application-defined value for the media item.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You can assign this value when you first create the media item, by specifying it in the <i>dwUserData</i> parameter of the <a href="https://msdn.microsoft.com/7dc2a7f3-81b4-46c6-b45e-44c6a20afc6b">IMFPMediaPlayer::CreateMediaItemFromURL</a> or <a href="https://msdn.microsoft.com/d647df89-b874-448e-ae41-ee3bcb55521f">IMFPMediaPlayer::CreateMediaItemFromObject</a> method. To update the value, call <a href="https://msdn.microsoft.com/17a10427-f13a-494c-bb68-a7722e8d9b6e">IMFPMediaItem::SetUserData</a>.

This method can be called after the player object is shut down.




## -see-also




<a href="https://msdn.microsoft.com/2839d256-bdaf-40cf-9f9d-46f9e2ce59e8">IMFPMediaItem</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

