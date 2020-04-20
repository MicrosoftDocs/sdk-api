---
UID: NN:strmif.IVMRVideoStreamControl
title: IVMRVideoStreamControl (strmif.h)
description: The IVMRVideoStreamControl interface is implemented on each input pin of the Video Mixing Renderer Filter 7 (VMR-7).helpviewer_keywords: ["IVMRVideoStreamControl","IVMRVideoStreamControl interface [DirectShow]","IVMRVideoStreamControl interface [DirectShow]","described","IVMRVideoStreamControlInterface","dshow.ivmrvideostreamcontrol","strmif/IVMRVideoStreamControl"]
old-location: dshow\ivmrvideostreamcontrol.htm
tech.root: DirectShow
ms.assetid: b42fa81e-99d7-4051-b909-2189581825d0
ms.date: 12/05/2018
ms.keywords: IVMRVideoStreamControl, IVMRVideoStreamControl interface [DirectShow], IVMRVideoStreamControl interface [DirectShow],described, IVMRVideoStreamControlInterface, dshow.ivmrvideostreamcontrol, strmif/IVMRVideoStreamControl
f1_keywords:
- strmif/IVMRVideoStreamControl
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
- IVMRVideoStreamControl
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRVideoStreamControl interface


## -description



The <code>IVMRVideoStreamControl</code> interface is implemented on each input pin of the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/video-mixing-renderer-filter-7">Video Mixing Renderer Filter 7</a> (VMR-7). The interface operates on the input stream represented by the pin. This interface is used by upstream filters (typically decoders) to get or set the active state of individual streams, or the source color key for the composited image. Applications in general should not use this interface.

The VMR-9 input pins expose the <a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nn-vmr9-ivmrvideostreamcontrol9">IVMRVideoStreamControl9</a> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRVideoStreamControl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRVideoStreamControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVMRVideoStreamControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrvideostreamcontrol-getcolorkey">GetColorKey</a>
</td>
<td align="left" width="63%">
Retrieves the source color key currently set for this stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrvideostreamcontrol-getstreamactivestate">GetStreamActiveState</a>
</td>
<td align="left" width="63%">
Retrieves the state of the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrvideostreamcontrol-setcolorkey">SetColorKey</a>
</td>
<td align="left" width="63%">
Sets the source color key that the VMR will use when compositing the video image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrvideostreamcontrol-setstreamactivestate">SetStreamActiveState</a>
</td>
<td align="left" width="63%">
Activates or inactivates an input stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

