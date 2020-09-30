---
UID: NF:strmif.IAMVideoCompression.get_WindowSize
title: IAMVideoCompression::get_WindowSize (strmif.h)
description: The get_WindowSize method retrieves the number of frames over which the compressor will maintain the average data rate.
helpviewer_keywords: ["IAMVideoCompression interface [DirectShow]","get_WindowSize method","IAMVideoCompression.get_WindowSize","IAMVideoCompression::get_WindowSize","IAMVideoCompressionget_WindowSize","dshow.iamvideocompression_get_windowsize","get_WindowSize","get_WindowSize method [DirectShow]","get_WindowSize method [DirectShow]","IAMVideoCompression interface","strmif/IAMVideoCompression::get_WindowSize"]
old-location: dshow\iamvideocompression_get_windowsize.htm
tech.root: dshow
ms.assetid: 1f12aa72-3468-4dca-a5f6-43f64f6d2f83
ms.date: 12/05/2018
ms.keywords: IAMVideoCompression interface [DirectShow],get_WindowSize method, IAMVideoCompression.get_WindowSize, IAMVideoCompression::get_WindowSize, IAMVideoCompressionget_WindowSize, dshow.iamvideocompression_get_windowsize, get_WindowSize, get_WindowSize method [DirectShow], get_WindowSize method [DirectShow],IAMVideoCompression interface, strmif/IAMVideoCompression::get_WindowSize
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
 - IAMVideoCompression::get_WindowSize
 - strmif/IAMVideoCompression::get_WindowSize
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
 - IAMVideoCompression.get_WindowSize
---

# IAMVideoCompression::get_WindowSize


## -description

The <code>get_WindowSize</code> method retrieves the number of frames over which the compressor will maintain the average data rate.



For example, assuming a data rate of 100K/sec and a frame rate of 10 frames per second, if the window size is 1, then every frame will be 10K or less. If the window size is 5, then every five consecutive frames will average 10K per frame, but individual frames may exceed this size.

The default window size is 1.

## -parameters

### -param pWindowSize [out]

Pointer to a variable that receives the window size, expressed as a number of frames.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamvideocompression">IAMVideoCompression Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamvideocompression-put_windowsize">IAMVideoCompression::put_WindowSize</a>