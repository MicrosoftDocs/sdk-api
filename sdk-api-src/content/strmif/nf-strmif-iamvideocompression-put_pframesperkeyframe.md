---
UID: NF:strmif.IAMVideoCompression.put_PFramesPerKeyFrame
title: IAMVideoCompression::put_PFramesPerKeyFrame (strmif.h)
description: The put_PFramesPerKeyFrame method sets the rate of predicted (P) frames per key frame.
helpviewer_keywords: ["IAMVideoCompression interface [DirectShow]","put_PFramesPerKeyFrame method","IAMVideoCompression.put_PFramesPerKeyFrame","IAMVideoCompression::put_PFramesPerKeyFrame","IAMVideoCompressionput_PFramesPerKeyFrame","dshow.iamvideocompression_put_pframesperkeyframe","put_PFramesPerKeyFrame","put_PFramesPerKeyFrame method [DirectShow]","put_PFramesPerKeyFrame method [DirectShow]","IAMVideoCompression interface","strmif/IAMVideoCompression::put_PFramesPerKeyFrame"]
old-location: dshow\iamvideocompression_put_pframesperkeyframe.htm
tech.root: dshow
ms.assetid: bf1dfc28-a6c7-4c0d-96ea-8cf417b13a10
ms.date: 12/05/2018
ms.keywords: IAMVideoCompression interface [DirectShow],put_PFramesPerKeyFrame method, IAMVideoCompression.put_PFramesPerKeyFrame, IAMVideoCompression::put_PFramesPerKeyFrame, IAMVideoCompressionput_PFramesPerKeyFrame, dshow.iamvideocompression_put_pframesperkeyframe, put_PFramesPerKeyFrame, put_PFramesPerKeyFrame method [DirectShow], put_PFramesPerKeyFrame method [DirectShow],IAMVideoCompression interface, strmif/IAMVideoCompression::put_PFramesPerKeyFrame
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMVideoCompression::put_PFramesPerKeyFrame
 - strmif/IAMVideoCompression::put_PFramesPerKeyFrame
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMVideoCompression.put_PFramesPerKeyFrame
---

# IAMVideoCompression::put_PFramesPerKeyFrame


## -description

The <code>put_PFramesPerKeyFrame</code> method sets the rate of predicted (P) frames per key frame.

## -parameters

### -param PFramesPerKeyFrame [in]

Specifies the number of P frames per key frame. If the value is negative, the filter will use the default rate.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

To determine if the filter supports this method, call the <a href="/windows/desktop/api/strmif/nf-strmif-iamvideocompression-getinfo">IAMVideoCompression::GetInfo</a> method and check for the <b>CompressionCaps_CanBFrame</b> flag in the <i>pCapabilities</i> parameter. The <b>GetInfo</b> method also returns the default P-frame rate.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamvideocompression">IAMVideoCompression Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamvideocompression-get_pframesperkeyframe">IAMVideoCompression::get_PFramesPerKeyFrame</a>