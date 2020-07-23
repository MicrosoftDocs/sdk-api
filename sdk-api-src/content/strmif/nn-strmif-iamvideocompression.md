---
UID: NN:strmif.IAMVideoCompression
title: IAMVideoCompression (strmif.h)
description: The IAMVideoCompression interface sets and retrieves video compression properties.
helpviewer_keywords: ["IAMVideoCompression","IAMVideoCompression interface [DirectShow]","IAMVideoCompression interface [DirectShow]","described","IAMVideoCompressionInterface","dshow.iamvideocompression","strmif/IAMVideoCompression"]
old-location: dshow\iamvideocompression.htm
tech.root: dshow
ms.assetid: 6b7d8a98-35b8-442f-bf51-9e66fd03e2c9
ms.date: 12/05/2018
ms.keywords: IAMVideoCompression, IAMVideoCompression interface [DirectShow], IAMVideoCompression interface [DirectShow],described, IAMVideoCompressionInterface, dshow.iamvideocompression, strmif/IAMVideoCompression
f1_keywords:
- strmif/IAMVideoCompression
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
- IAMVideoCompression
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMVideoCompression interface


## -description



The <b>IAMVideoCompression</b> interface sets and retrieves video compression properties. It is supported by some video compression filters, and also by some video capture filters that output compressed video. Filters that support this interface expose it through their output pins.

An application can use this interface to control how video is compressed, including characteristics such as the key-frame rate or the compression quality.

A filter that supports this interface might not support every method. Use the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamvideocompression-getinfo">IAMVideoCompression::GetInfo</a> method to determine which methods the filter supports.

<div class="alert"><b>Note</b>  To use this interface on a capture filter, you might need to connect the filter to another filter in the graph.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMVideoCompression</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMVideoCompression</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMVideoCompression</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamvideocompression-get_keyframerate">get_KeyFrameRate</a>
</td>
<td align="left" width="63%">
Retrieves the key-frame rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamvideocompression-get_pframesperkeyframe">get_PFramesPerKeyFrame</a>
</td>
<td align="left" width="63%">
Retrieves the P frame frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamvideocompression-get_quality">get_Quality</a>
</td>
<td align="left" width="63%">
Retrieves the compression quality.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamvideocompression-get_windowsize">get_WindowSize</a>
</td>
<td align="left" width="63%">
Retrieves the number of frames over which the compressor must maintain an average data rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamvideocompression-getinfo">GetInfo</a>
</td>
<td align="left" width="63%">
Retrieves information about the filter's compression properties, including capabilities and default values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamvideocompression-overrideframesize">OverrideFrameSize</a>
</td>
<td align="left" width="63%">
Overrides a particular frame's data rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamvideocompression-overridekeyframe">OverrideKeyFrame</a>
</td>
<td align="left" width="63%">
Forces a particular frame to be a key frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamvideocompression-put_keyframerate">put_KeyFrameRate</a>
</td>
<td align="left" width="63%">
Sets the key-frame rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamvideocompression-put_pframesperkeyframe">put_PFramesPerKeyFrame</a>
</td>
<td align="left" width="63%">
Sets the predicted (P) frame frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamvideocompression-put_quality">put_Quality</a>
</td>
<td align="left" width="63%">
Sets the compression quality.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamvideocompression-put_windowsize">put_WindowSize</a>
</td>
<td align="left" width="63%">
Sets the number of frames over which the compressor must maintain an average data rate.

</td>
</tr>
</table> 


## -remarks



For Windows Driver Model (WDM) devices, the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/wdm-video-capture-filter">WDM Video Capture Filter</a> automatically exposes this interface if the WDM driver supports the <a href="https://docs.microsoft.com/windows-hardware/drivers/stream/propsetid-vidcap-videocompression">PROPSETID_VIDCAP_VIDEOCOMPRESSION</a> property set. For more information, see the <a href="https://msdn.microsoft.com/library/ff554690(VS.85).aspx">Windows Driver Kit (WDK)</a> documentation.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/interfaces">Interfaces</a>
 

 

