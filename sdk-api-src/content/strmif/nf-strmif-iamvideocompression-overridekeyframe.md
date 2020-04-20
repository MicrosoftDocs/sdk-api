---
UID: NF:strmif.IAMVideoCompression.OverrideKeyFrame
title: IAMVideoCompression::OverrideKeyFrame (strmif.h)
description: The OverrideKeyFrame method instructs the filter to compress a particular frame as a key frame.helpviewer_keywords: ["IAMVideoCompression interface [DirectShow]","OverrideKeyFrame method","IAMVideoCompression.OverrideKeyFrame","IAMVideoCompression::OverrideKeyFrame","IAMVideoCompressionOverrideKeyFrame","OverrideKeyFrame","OverrideKeyFrame method [DirectShow]","OverrideKeyFrame method [DirectShow]","IAMVideoCompression interface","dshow.iamvideocompression_overridekeyframe","strmif/IAMVideoCompression::OverrideKeyFrame"]
old-location: dshow\iamvideocompression_overridekeyframe.htm
tech.root: DirectShow
ms.assetid: 2e8e52b9-cc66-42f5-a0ea-110188bfcf8b
ms.date: 12/05/2018
ms.keywords: IAMVideoCompression interface [DirectShow],OverrideKeyFrame method, IAMVideoCompression.OverrideKeyFrame, IAMVideoCompression::OverrideKeyFrame, IAMVideoCompressionOverrideKeyFrame, OverrideKeyFrame, OverrideKeyFrame method [DirectShow], OverrideKeyFrame method [DirectShow],IAMVideoCompression interface, dshow.iamvideocompression_overridekeyframe, strmif/IAMVideoCompression::OverrideKeyFrame
f1_keywords:
- strmif/IAMVideoCompression.OverrideKeyFrame
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
- IAMVideoCompression.OverrideKeyFrame
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMVideoCompression::OverrideKeyFrame


## -description



The <code>OverrideKeyFrame</code> method instructs the filter to compress a particular frame as a key frame.




## -parameters




### -param FrameNumber [in]

Specifies the frame number. The first frame that the filter delivers is numbered zero.


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



If the filter supports this method, you can use it to override the normal key-frame distribution for a particular frame. After the filter creates a key frame, it might reset its count to determine when the next key frame should occur. For example, if the key-frame rate is 10, and an application uses this method to force frame 5 as a key frame, the filter might wait another 10 frames (until frame 15) before it creates the next key frame.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamvideocompression">IAMVideoCompression Interface</a>
 

 

