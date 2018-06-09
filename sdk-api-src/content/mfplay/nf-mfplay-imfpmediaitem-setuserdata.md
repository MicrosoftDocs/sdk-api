---
UID: NF:mfplay.IMFPMediaItem.SetUserData
title: IMFPMediaItem::SetUserData
author: windows-sdk-content
description: Stores an application-defined value in the media item.
old-location: mf\imfpmediaitem_setuserdata.htm
old-project: medfound
ms.assetid: 17a10427-f13a-494c-bb68-a7722e8d9b6e
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: IMFPMediaItem interface [Media Foundation],SetUserData method, IMFPMediaItem.SetUserData, IMFPMediaItem::SetUserData, SetUserData, SetUserData method [Media Foundation], SetUserData method [Media Foundation],IMFPMediaItem interface, mf.imfpmediaitem_setuserdata, mfplay/IMFPMediaItem::SetUserData
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
 - IMFPMediaItem.SetUserData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFPMediaItem::SetUserData


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Stores an application-defined value in the media item.


## -parameters




### -param dwUserData [in]

The application-defined value.


## -returns



This method can return one of these values.




## -remarks



This method can be called after the player object is shut down.




## -see-also




<a href="https://msdn.microsoft.com/2839d256-bdaf-40cf-9f9d-46f9e2ce59e8">IMFPMediaItem</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

