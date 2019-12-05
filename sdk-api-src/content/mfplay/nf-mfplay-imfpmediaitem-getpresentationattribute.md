---
UID: NF:mfplay.IMFPMediaItem.GetPresentationAttribute
title: IMFPMediaItem::GetPresentationAttribute (mfplay.h)
description: Queries the media item for a presentation attribute.
old-location: mf\imfpmediaitem_getpresentationattribute.htm
tech.root: medfound
ms.assetid: d6600009-a8da-4464-9df7-08f20a1a6b15
ms.date: 12/05/2018
ms.keywords: GetPresentationAttribute, GetPresentationAttribute method [Media Foundation], GetPresentationAttribute method [Media Foundation],IMFPMediaItem interface, IMFPMediaItem interface [Media Foundation],GetPresentationAttribute method, IMFPMediaItem.GetPresentationAttribute, IMFPMediaItem::GetPresentationAttribute, mf.imfpmediaitem_getpresentationattribute, mfplay/IMFPMediaItem::GetPresentationAttribute
ms.topic: method
f1_keywords:
- mfplay/IMFPMediaItem.GetPresentationAttribute
dev_langs:
- c++
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
- IMFPMediaItem.GetPresentationAttribute
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFPMediaItem::GetPresentationAttribute


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://docs.microsoft.com/windows/desktop/medfound/media-session">Media Session</a> for playback.</div>
<div> </div>


Queries the media item for a presentation attribute.


## -parameters




### -param guidMFAttribute [in]

GUID that identifies the attribute value to query.

For a list of presentation attributes, see <a href="https://docs.microsoft.com/windows/desktop/medfound/presentation-descriptor-attributes">Presentation Descriptor Attributes</a>.


### -param pvValue [out]

Pointer to a <b>PROPVARIANT</b> that receives the value. The method fills the <b>PROPVARIANT</b> with a copy of the stored value. Call <b>PropVariantClear</b> to free the memory allocated by the method.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Presentation attributes describe the presentation as a whole. To get an attribute that applies to an individual stream within the presentation, call <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getstreamattribute">IMFPMediaItem::GetStreamAttribute</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem">IMFPMediaItem</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>
 

 

