---
UID: NF:strmif.IAMVideoCompression.get_KeyFrameRate
title: IAMVideoCompression::get_KeyFrameRate (strmif.h)
description: The get_KeyFrameRate method retrieves the current key-frame rate.
helpviewer_keywords: ["IAMVideoCompression interface [DirectShow]","get_KeyFrameRate method","IAMVideoCompression.get_KeyFrameRate","IAMVideoCompression::get_KeyFrameRate","IAMVideoCompressionget_KeyFrameRate","dshow.iamvideocompression_get_keyframerate","get_KeyFrameRate","get_KeyFrameRate method [DirectShow]","get_KeyFrameRate method [DirectShow]","IAMVideoCompression interface","strmif/IAMVideoCompression::get_KeyFrameRate"]
old-location: dshow\iamvideocompression_get_keyframerate.htm
tech.root: dshow
ms.assetid: af73cfaa-3297-44a7-96a7-8805aad057e2
ms.date: 12/05/2018
ms.keywords: IAMVideoCompression interface [DirectShow],get_KeyFrameRate method, IAMVideoCompression.get_KeyFrameRate, IAMVideoCompression::get_KeyFrameRate, IAMVideoCompressionget_KeyFrameRate, dshow.iamvideocompression_get_keyframerate, get_KeyFrameRate, get_KeyFrameRate method [DirectShow], get_KeyFrameRate method [DirectShow],IAMVideoCompression interface, strmif/IAMVideoCompression::get_KeyFrameRate
f1_keywords:
- strmif/IAMVideoCompression.get_KeyFrameRate
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IAMVideoCompression.get_KeyFrameRate
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMVideoCompression::get_KeyFrameRate


## -description



The <code>get_KeyFrameRate</code> method retrieves the current key-frame rate.




## -parameters




### -param pKeyFrameRate [out]

Pointer to a variable that receives the current key-frame rate. If the value is negative, the filter will use the default key-frame rate. If the value is zero, only the first frame is a key frame.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



The key-frame rate is the number of frames per key frame. For example, if the rate is 15, then a key frame occurs every 15 frames.

To determine if the filter supports this method, call the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamvideocompression-getinfo">IAMVideoCompression::GetInfo</a> method and check for the <b>CompressionCaps_CanKeyFrame</b> flag in the <i>pCapabilities</i> parameter. The <b>GetInfo</b> method also returns the default key-frame rate.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamvideocompression">IAMVideoCompression Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamvideocompression-put_keyframerate">IAMVideoCompression::put_KeyFrameRate</a>
 

 

