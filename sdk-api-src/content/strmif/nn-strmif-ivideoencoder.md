---
UID: NN:strmif.IVideoEncoder
title: IVideoEncoder (strmif.h)
author: windows-sdk-content
description: The IVideoEncoder interface is optionally exposed by video encoder filters.
old-location: dshow\ivideoencoder.htm
tech.root: DirectShow
ms.assetid: 9264f7a2-b2d4-4449-913b-f1e5ecb40cac
ms.author: windowssdkdev
ms.date: 12/05/2018
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
ms.custom: 19H1
---

# IVideoEncoder interface


## -description


<p class="CCE_Message">[<b>IVideoEncoder</b> may be altered or unavailable in 

subsequent versions.]

The <b>IVideoEncoder</b> interface is optionally exposed by video encoder filters.


## -remarks



The original purpose of this interface was to enable application to determine whether a filter was a video decoder, by calling <b>QueryInterface</b> for the <b>IVideoEncoder</b> interface. The application could then use the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iencoderapi">IEncoderAPI</a> interface (which <b>IVideoEncoder</b> inherits) to set properties on the encoder. However, <b>IEncoderAPI</b> is deprecated. Encoder filters should expose <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI</a> instead, and applications should use <b>ICodecAPI</b> to configure encoders.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/deprecated-interfaces">Deprecated Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iencoderapi">IEncoderAPI</a>
 

 

