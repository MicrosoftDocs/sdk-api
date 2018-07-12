---
UID: NF:mfplay.IMFPMediaItem.GetMetadata
title: IMFPMediaItem::GetMetadata
author: windows-sdk-content
description: Gets a property store that contains metadata for the source, such as author or title.
old-location: mf\imfpmediaitem_getmetadata.htm
old-project: medfound
ms.assetid: 212d468f-de5e-4a55-aaa4-ed487bbf6a00
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetMetadata, GetMetadata method [Media Foundation], GetMetadata method [Media Foundation],IMFPMediaItem interface, IMFPMediaItem interface [Media Foundation],GetMetadata method, IMFPMediaItem.GetMetadata, IMFPMediaItem::GetMetadata, mf.imfpmediaitem_getmetadata, mfplay/IMFPMediaItem::GetMetadata
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
 - IMFPMediaItem.GetMetadata
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFPMediaItem::GetMetadata


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Gets a property store that contains metadata for the source, such as author or title.


## -parameters




### -param ppMetadataStore [out]

Receives a pointer to the <b>IPropertyStore</b> interface of a read-only property store. The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2839d256-bdaf-40cf-9f9d-46f9e2ce59e8">IMFPMediaItem</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

