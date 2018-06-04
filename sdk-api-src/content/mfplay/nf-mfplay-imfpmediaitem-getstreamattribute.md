---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IMFPMediaItem::GetStreamAttribute


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Queries the media item for a stream attribute.


## -parameters




### -param dwStreamIndex [in]

Zero-based index of the stream. To get the number of streams, call <a href="https://msdn.microsoft.com/65a3cfc8-9171-4206-b1b6-54bb0d3ecdd1">IMFPMediaItem::GetNumberOfStreams</a>.


### -param guidMFAttribute [in]

GUID that identifies the attribute value to query. Possible values are listed in the following topics:

<ul>
<li>
<a href="https://msdn.microsoft.com/1364d7c5-67e8-49b6-8038-d6d4ea03fb7d">Stream Descriptor Attributes</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e84ba3f6-4857-4340-baca-5847650ea7b8">Media Type Attributes</a>
</li>
</ul>

### -param pvValue [out]

Pointer to a <b>PROPVARIANT</b> that receives the value. The method fills the <b>PROPVARIANT</b> with a copy of the stored value. Call <b>PropVariantClear</b> to free the memory allocated by this method.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Stream attributes describe an individual stream (audio, video, or other) within the presentation. To get an attribute that applies to the entire presentation, call <a href="https://msdn.microsoft.com/d6600009-a8da-4464-9df7-08f20a1a6b15">IMFPMediaItem::GetPresentationAttribute</a>.




## -see-also




<a href="https://msdn.microsoft.com/2839d256-bdaf-40cf-9f9d-46f9e2ce59e8">IMFPMediaItem</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

