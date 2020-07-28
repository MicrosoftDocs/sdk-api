---
UID: NF:strmif.IAMVideoCompression.OverrideFrameSize
title: IAMVideoCompression::OverrideFrameSize (strmif.h)
description: The OverrideFrameSize method overrides the frame size of a specified frame.
helpviewer_keywords: ["IAMVideoCompression interface [DirectShow]","OverrideFrameSize method","IAMVideoCompression.OverrideFrameSize","IAMVideoCompression::OverrideFrameSize","IAMVideoCompressionOverrideFrameSize","OverrideFrameSize","OverrideFrameSize method [DirectShow]","OverrideFrameSize method [DirectShow]","IAMVideoCompression interface","dshow.iamvideocompression_overrideframesize","strmif/IAMVideoCompression::OverrideFrameSize"]
old-location: dshow\iamvideocompression_overrideframesize.htm
tech.root: dshow
ms.assetid: 19f5d231-965e-4b0a-bd0b-e85b03d79c71
ms.date: 12/05/2018
ms.keywords: IAMVideoCompression interface [DirectShow],OverrideFrameSize method, IAMVideoCompression.OverrideFrameSize, IAMVideoCompression::OverrideFrameSize, IAMVideoCompressionOverrideFrameSize, OverrideFrameSize, OverrideFrameSize method [DirectShow], OverrideFrameSize method [DirectShow],IAMVideoCompression interface, dshow.iamvideocompression_overrideframesize, strmif/IAMVideoCompression::OverrideFrameSize
f1_keywords:
- strmif/IAMVideoCompression.OverrideFrameSize
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
- IAMVideoCompression.OverrideFrameSize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMVideoCompression::OverrideFrameSize


## -description



The <code>OverrideFrameSize</code> method overrides the frame size of a specified frame.




## -parameters




### -param FrameNumber [in]

Specifies the frame number. The first frame that the filter delivers is numbered zero.


### -param Size [in]

Specifies the maximum size of the specified frame, in bytes.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
</table>
 




## -remarks



If the filter supports this method, the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamvideocompression-getinfo">IAMVideoCompression::GetInfo</a> method will return the <b>CompressionCaps_CanCrunch</b> flag in the <i>pCapabilities</i> parameter. However, this flag can also indicate that the filter supports setting the bit rate, so it does not guarantee that the <code>OverrideFrameSize</code> method is supported.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-compressioncaps">CompressionCaps Enumeration</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamvideocompression">IAMVideoCompression Interface</a>
 

 

