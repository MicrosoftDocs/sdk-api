---
UID: NF:mfplay.IMFPMediaItem.GetMetadata
title: IMFPMediaItem::GetMetadata (mfplay.h)
author: windows-sdk-content
description: Gets a property store that contains metadata for the source, such as author or title.
old-location: mf\imfpmediaitem_getmetadata.htm
tech.root: medfound
ms.assetid: 212d468f-de5e-4a55-aaa4-ed487bbf6a00
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetMetadata, GetMetadata method [Media Foundation], GetMetadata method [Media Foundation],IMFPMediaItem interface, IMFPMediaItem interface [Media Foundation],GetMetadata method, IMFPMediaItem.GetMetadata, IMFPMediaItem::GetMetadata, mf.imfpmediaitem_getmetadata, mfplay/IMFPMediaItem::GetMetadata
ms.topic: method
f1_keywords: 
 - "mfplay/IMFPMediaItem.GetMetadata"
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
 - IMFPMediaItem.GetMetadata
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFPMediaItem::GetMetadata


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://docs.microsoft.com/windows/desktop/medfound/media-session">Media Session</a> for playback.</div>
<div> </div>


Gets a property store that contains metadata for the source, such as author or title.


## -parameters




### -param ppMetadataStore [out]

Receives a pointer to the <b>IPropertyStore</b> interface of a read-only property store. The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem">IMFPMediaItem</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>
 

 

