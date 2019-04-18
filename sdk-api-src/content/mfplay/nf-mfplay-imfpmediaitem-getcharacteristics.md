---
UID: NF:mfplay.IMFPMediaItem.GetCharacteristics
title: IMFPMediaItem::GetCharacteristics (mfplay.h)
author: windows-sdk-content
description: Gets various flags that describe the media item.
old-location: mf\imfpmediaitem_getcharacteristics.htm
tech.root: medfound
ms.assetid: 9fe65644-c7a0-4af5-9765-f933215f5f83
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCharacteristics, GetCharacteristics method [Media Foundation], GetCharacteristics method [Media Foundation],IMFPMediaItem interface, IMFPMediaItem interface [Media Foundation],GetCharacteristics method, IMFPMediaItem.GetCharacteristics, IMFPMediaItem::GetCharacteristics, mf.imfpmediaitem_getcharacteristics, mfplay/IMFPMediaItem::GetCharacteristics
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
 - IMFPMediaItem.GetCharacteristics
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFPMediaItem::GetCharacteristics


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Gets various flags that describe the media item.


## -parameters




### -param pCharacteristics [out]

Receives a bitwise <b>OR</b> of flags from the <a href="https://msdn.microsoft.com/7bbb45e6-717d-413c-95fd-db730ab960ff">_MFP_MEDIAITEM_CHARACTERISTICS</a> enumeration.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2839d256-bdaf-40cf-9f9d-46f9e2ce59e8">IMFPMediaItem</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

