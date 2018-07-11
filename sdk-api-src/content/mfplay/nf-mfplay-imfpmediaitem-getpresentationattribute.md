---
UID: NF:mfplay.IMFPMediaItem.GetPresentationAttribute
title: IMFPMediaItem::GetPresentationAttribute
author: windows-sdk-content
description: Queries the media item for a presentation attribute.
old-location: mf\imfpmediaitem_getpresentationattribute.htm
old-project: medfound
ms.assetid: d6600009-a8da-4464-9df7-08f20a1a6b15
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetPresentationAttribute, GetPresentationAttribute method [Media Foundation], GetPresentationAttribute method [Media Foundation],IMFPMediaItem interface, IMFPMediaItem interface [Media Foundation],GetPresentationAttribute method, IMFPMediaItem.GetPresentationAttribute, IMFPMediaItem::GetPresentationAttribute, mf.imfpmediaitem_getpresentationattribute, mfplay/IMFPMediaItem::GetPresentationAttribute
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
 - IMFPMediaItem.GetPresentationAttribute
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFPMediaItem::GetPresentationAttribute


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Queries the media item for a presentation attribute.


## -parameters




### -param guidMFAttribute [in]

GUID that identifies the attribute value to query.

For a list of presentation attributes, see <a href="https://msdn.microsoft.com/2a092a6a-956b-4c1f-955f-529ec08665fe">Presentation Descriptor Attributes</a>.


### -param pvValue [out]

Pointer to a <b>PROPVARIANT</b> that receives the value. The method fills the <b>PROPVARIANT</b> with a copy of the stored value. Call <b>PropVariantClear</b> to free the memory allocated by the method.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Presentation attributes describe the presentation as a whole. To get an attribute that applies to an individual stream within the presentation, call <a href="https://msdn.microsoft.com/8c40ce33-2077-4e7b-8a1c-c080e82df078">IMFPMediaItem::GetStreamAttribute</a>.




## -see-also




<a href="https://msdn.microsoft.com/2839d256-bdaf-40cf-9f9d-46f9e2ce59e8">IMFPMediaItem</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

