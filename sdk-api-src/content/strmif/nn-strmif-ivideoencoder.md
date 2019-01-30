---
UID: NN:strmif.IVideoEncoder
title: IVideoEncoder
author: windows-sdk-content
description: The IVideoEncoder interface is optionally exposed by video encoder filters.
old-location: dshow\ivideoencoder.htm
tech.root: DirectShow
ms.assetid: 9264f7a2-b2d4-4449-913b-f1e5ecb40cac
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVideoEncoder, IVideoEncoder interface [DirectShow], IVideoEncoder interface [DirectShow],described, dshow.ivideoencoder, strmif/IVideoEncoder
ms.topic: interface
req.header: strmif.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmif.h
api_name:
 - IVideoEncoder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVideoEncoder interface


## -description


<p class="CCE_Message">[<b>IVideoEncoder</b> may be altered or unavailable in 

subsequent versions.]

The <b>IVideoEncoder</b> interface is optionally exposed by video encoder filters.


## -remarks



The original purpose of this interface was to enable application to determine whether a filter was a video decoder, by calling <b>QueryInterface</b> for the <b>IVideoEncoder</b> interface. The application could then use the <a href="https://msdn.microsoft.com/823b79a1-1bf5-4aab-80dd-0e77ba950127">IEncoderAPI</a> interface (which <b>IVideoEncoder</b> inherits) to set properties on the encoder. However, <b>IEncoderAPI</b> is deprecated. Encoder filters should expose <a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI</a> instead, and applications should use <b>ICodecAPI</b> to configure encoders.




## -see-also




<a href="https://msdn.microsoft.com/5b798477-9b36-4f59-b9cc-2938b5e4009f">Deprecated Interfaces</a>



<a href="https://msdn.microsoft.com/823b79a1-1bf5-4aab-80dd-0e77ba950127">IEncoderAPI</a>
 

 

