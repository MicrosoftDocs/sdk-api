---
UID: NN:strmif.IVMRImageCompositor
title: IVMRImageCompositor (strmif.h)
description: The IVMRImageCompositor interface is implemented by the default compositor for the Video Mixing Renderer Filter 7 (VMR-7).helpviewer_keywords: ["IVMRImageCompositor","IVMRImageCompositor interface [DirectShow]","IVMRImageCompositor interface [DirectShow]","described","IVMRImageCompositorInterface","dshow.ivmrimagecompositor","strmif/IVMRImageCompositor"]
old-location: dshow\ivmrimagecompositor.htm
tech.root: DirectShow
ms.assetid: d905e871-c156-4140-bb3f-a19fa0cd79be
ms.date: 12/05/2018
ms.keywords: IVMRImageCompositor, IVMRImageCompositor interface [DirectShow], IVMRImageCompositor interface [DirectShow],described, IVMRImageCompositorInterface, dshow.ivmrimagecompositor, strmif/IVMRImageCompositor
f1_keywords:
- strmif/IVMRImageCompositor
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
- IVMRImageCompositor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRImageCompositor interface


## -description



The <code>IVMRImageCompositor</code> interface is implemented by the default compositor for the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/video-mixing-renderer-filter-7">Video Mixing Renderer Filter 7</a> (VMR-7). It must also be implemented by any plug-in compositor that an application provides for the VMR-7. The VMR-7 calls the methods on this interface to inform the Compositor that it should composite the incoming video frames into a single output frame. Applications do not use this interface.

For the VMR-9, use the <a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nn-vmr9-ivmrimagecompositor9">IVMRImageCompositor9</a> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRImageCompositor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRImageCompositor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVMRImageCompositor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrimagecompositor-compositeimage">CompositeImage</a>
</td>
<td align="left" width="63%">
Composites the current frames available in each input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrimagecompositor-initcompositiontarget">InitCompositionTarget</a>
</td>
<td align="left" width="63%">
Informs the compositor that a new composition target has been created.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrimagecompositor-setstreammediatype">SetStreamMediaType</a>
</td>
<td align="left" width="63%">
Sets the media type for the input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrimagecompositor-termcompositiontarget">TermCompositionTarget</a>
</td>
<td align="left" width="63%">
Informs the compositor that the current composition target is being replaced.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

