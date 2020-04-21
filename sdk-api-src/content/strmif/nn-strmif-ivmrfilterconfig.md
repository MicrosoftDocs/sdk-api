---
UID: NN:strmif.IVMRFilterConfig
title: IVMRFilterConfig (strmif.h)
description: The IVMRFilterConfig interface is used to configure the operating mode and video rendering mechanisms of the Video Mixing Renderer Filter 7 (VMR-7).helpviewer_keywords: ["IVMRFilterConfig","IVMRFilterConfig interface [DirectShow]","IVMRFilterConfig interface [DirectShow]","described","IVMRFilterConfigInterface","dshow.ivmrfilterconfig","strmif/IVMRFilterConfig"]
old-location: dshow\ivmrfilterconfig.htm
tech.root: DirectShow
ms.assetid: 3ea7bb41-1f5f-496f-bdf4-776ec9f28876
ms.date: 12/05/2018
ms.keywords: IVMRFilterConfig, IVMRFilterConfig interface [DirectShow], IVMRFilterConfig interface [DirectShow],described, IVMRFilterConfigInterface, dshow.ivmrfilterconfig, strmif/IVMRFilterConfig
f1_keywords:
- strmif/IVMRFilterConfig
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
- IVMRFilterConfig
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRFilterConfig interface


## -description



The <code>IVMRFilterConfig</code> interface is used to configure the operating mode and video rendering mechanisms of the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/video-mixing-renderer-filter-7">Video Mixing Renderer Filter 7</a> (VMR-7). For the VMR-9, use the <a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nn-vmr9-ivmrfilterconfig9">IVMRFilterConfig9</a> interface.

Applications must add the VMR to the graph and configure it before connecting it to any upstream filters (for example, in a call to <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-igraphbuilder-renderfile">IGraphBuilder::RenderFile</a>). Once a filter has been connected to the VMR, the VMR's configuration is locked and all future attempts to alter it fail.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRFilterConfig</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRFilterConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVMRFilterConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrfilterconfig-getnumberofstreams">GetNumberOfStreams</a>
</td>
<td align="left" width="63%">
Retrieves the number of input streams being mixed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrfilterconfig-getrenderingmode">GetRenderingMode</a>
</td>
<td align="left" width="63%">
Retrieves the rendering mode currently being used by the VMR.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrfilterconfig-getrenderingprefs">GetRenderingPrefs</a>
</td>
<td align="left" width="63%">
Retrieves the current set of rendering preferences being used by the VMR.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrfilterconfig-setimagecompositor">SetImageCompositor</a>
</td>
<td align="left" width="63%">
Installs an application-provided image compositor object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams">SetNumberOfStreams</a>
</td>
<td align="left" width="63%">
Sets the number of streams to be mixed and instructs the VMR to go into mixer mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrfilterconfig-setrenderingmode">SetRenderingMode</a>
</td>
<td align="left" width="63%">
Sets the rendering mode used by the VMR.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrfilterconfig-setrenderingprefs">SetRenderingPrefs</a>
</td>
<td align="left" width="63%">
Sets various application preferences related to video rendering.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

