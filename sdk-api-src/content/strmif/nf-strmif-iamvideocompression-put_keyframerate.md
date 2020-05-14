---
UID: NF:strmif.IAMVideoCompression.put_KeyFrameRate
title: IAMVideoCompression::put_KeyFrameRate (strmif.h)
description: The put_KeyFrameRate method sets the key-frame rate.helpviewer_keywords: ["IAMVideoCompression interface [DirectShow]","put_KeyFrameRate method","IAMVideoCompression.put_KeyFrameRate","IAMVideoCompression::put_KeyFrameRate","IAMVideoCompressionput_KeyFrameRate","dshow.iamvideocompression_put_keyframerate","put_KeyFrameRate","put_KeyFrameRate method [DirectShow]","put_KeyFrameRate method [DirectShow]","IAMVideoCompression interface","strmif/IAMVideoCompression::put_KeyFrameRate"]
old-location: dshow\iamvideocompression_put_keyframerate.htm
tech.root: DirectShow
ms.assetid: dc229333-3524-4228-ab13-a6e9619643fd
ms.date: 12/05/2018
ms.keywords: IAMVideoCompression interface [DirectShow],put_KeyFrameRate method, IAMVideoCompression.put_KeyFrameRate, IAMVideoCompression::put_KeyFrameRate, IAMVideoCompressionput_KeyFrameRate, dshow.iamvideocompression_put_keyframerate, put_KeyFrameRate, put_KeyFrameRate method [DirectShow], put_KeyFrameRate method [DirectShow],IAMVideoCompression interface, strmif/IAMVideoCompression::put_KeyFrameRate
f1_keywords:
- strmif/IAMVideoCompression.put_KeyFrameRate
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
- IAMVideoCompression.put_KeyFrameRate
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMVideoCompression::put_KeyFrameRate


## -description



The <code>put_KeyFrameRate</code> method sets the key-frame rate.




## -parameters




### -param KeyFrameRate [in]

Desired key-frame rate. If the value is negative, the filter will use the default key-frame rate. If the value is zero, only the first frame will be a key frame.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



To determine if the filter supports this method, call the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamvideocompression-getinfo">IAMVideoCompression::GetInfo</a> method and check for the <b>CompressionCaps_CanKeyFrame</b> flag in the <i>pCapabilities</i> parameter. The <b>GetInfo</b> method also returns the default key-frame rate.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamvideocompression">IAMVideoCompression Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamvideocompression-get_keyframerate">IAMVideoCompression::get_KeyFrameRate</a>
 

 

