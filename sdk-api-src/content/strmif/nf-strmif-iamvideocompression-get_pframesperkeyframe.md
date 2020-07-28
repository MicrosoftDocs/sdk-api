---
UID: NF:strmif.IAMVideoCompression.get_PFramesPerKeyFrame
title: IAMVideoCompression::get_PFramesPerKeyFrame (strmif.h)
description: The get_PFramesPerKeyFrame method retrieves the rate of predicted (P) frames per key frame.
helpviewer_keywords: ["IAMVideoCompression interface [DirectShow]","get_PFramesPerKeyFrame method","IAMVideoCompression.get_PFramesPerKeyFrame","IAMVideoCompression::get_PFramesPerKeyFrame","IAMVideoCompressionget_PFramesPerKeyFrame","dshow.iamvideocompression_get_pframesperkeyframe","get_PFramesPerKeyFrame","get_PFramesPerKeyFrame method [DirectShow]","get_PFramesPerKeyFrame method [DirectShow]","IAMVideoCompression interface","strmif/IAMVideoCompression::get_PFramesPerKeyFrame"]
old-location: dshow\iamvideocompression_get_pframesperkeyframe.htm
tech.root: dshow
ms.assetid: 621292dd-42d9-4458-8971-929db39ed8b9
ms.date: 12/05/2018
ms.keywords: IAMVideoCompression interface [DirectShow],get_PFramesPerKeyFrame method, IAMVideoCompression.get_PFramesPerKeyFrame, IAMVideoCompression::get_PFramesPerKeyFrame, IAMVideoCompressionget_PFramesPerKeyFrame, dshow.iamvideocompression_get_pframesperkeyframe, get_PFramesPerKeyFrame, get_PFramesPerKeyFrame method [DirectShow], get_PFramesPerKeyFrame method [DirectShow],IAMVideoCompression interface, strmif/IAMVideoCompression::get_PFramesPerKeyFrame
f1_keywords:
- strmif/IAMVideoCompression.get_PFramesPerKeyFrame
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
- IAMVideoCompression.get_PFramesPerKeyFrame
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMVideoCompression::get_PFramesPerKeyFrame


## -description



The <code>get_PFramesPerKeyFrame</code> method retrieves the rate of predicted (P) frames per key frame.




## -parameters




### -param pPFramesPerKeyFrame [out]

Pointer to a variable that receives the number of P frames per key frame. If the value is negative, the filter will use the default rate.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



To determine if the filter supports this method, call the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamvideocompression-getinfo">IAMVideoCompression::GetInfo</a> method and check for the <b>CompressionCaps_CanBFrame</b> flag in the <i>pCapabilities</i> parameter. The <b>GetInfo</b> method also returns the default P-frame rate.

P frames are used in MPEG compression; in general, this property does not apply to other compression formats. For example, suppose a key frame occurs once every 10 frames, and there are three P frames per key frame. The P frames will be spaced evenly between the key frames. The remaining six frames are bidirectional (B) frames.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamvideocompression">IAMVideoCompression Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamvideocompression-put_keyframerate">IAMVideoCompression::put_KeyFrameRate</a>
 

 

