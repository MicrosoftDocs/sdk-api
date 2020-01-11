---
UID: NN:vmr9.IVMRFilterConfig9
title: IVMRFilterConfig9 (vmr9.h)
description: The IVMRFilterConfig9 interface is implemented by the Video Mixing Renderer Filter 9.
old-location: dshow\ivmrfilterconfig9.htm
tech.root: DirectShow
ms.assetid: 089e44c8-6a27-410d-aad5-08816bd4f915
ms.date: 12/05/2018
ms.keywords: IVMRFilterConfig9, IVMRFilterConfig9 interface [DirectShow], IVMRFilterConfig9 interface [DirectShow],described, IVMRFilterConfig9Interface, dshow.ivmrfilterconfig9, vmr9/IVMRFilterConfig9
f1_keywords:
- vmr9/IVMRFilterConfig9
dev_langs:
- c++
req.header: vmr9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
- IVMRFilterConfig9
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRFilterConfig9 interface


## -description



The <code>IVMRFilterConfig9</code> interface is implemented by the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/video-mixing-renderer-filter-9">Video Mixing Renderer Filter 9</a>. Applications use this interface to configure the VMR's operating mode and video rendering mechanisms. Applications must add the VMR to the graph and configure it before it is connected to any upstream filters (for example, in a call to <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-igraphbuilder-renderfile">IGraphBuilder::RenderFile</a>). Once a filter has been connected to the VMR, the VMR's configuration is locked and all future attempts to alter it fail.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRFilterConfig9</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRFilterConfig9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVMRFilterConfig9</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrfilterconfig9-getnumberofstreams">GetNumberOfStreams</a>
</td>
<td align="left" width="63%">
Retrieves the number of input streams being mixed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrfilterconfig9-getrenderingmode">GetRenderingMode</a>
</td>
<td align="left" width="63%">
Retrieves the rendering mode currently being used by the VMR.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrfilterconfig9-getrenderingprefs">GetRenderingPrefs</a>
</td>
<td align="left" width="63%">
Retrieves the current set of rendering preferences being used by the VMR.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrfilterconfig9-setimagecompositor">SetImageCompositor</a>
</td>
<td align="left" width="63%">
Installs an application-provided image compositor object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrfilterconfig9-setnumberofstreams">SetNumberOfStreams</a>
</td>
<td align="left" width="63%">
Sets the number of streams to be mixed and instructs the VMR to go into mixer mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode">SetRenderingMode</a>
</td>
<td align="left" width="63%">
Sets the rendering mode used by the VMR.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingprefs">SetRenderingPrefs</a>
</td>
<td align="left" width="63%">
Sets various application preferences related to video rendering.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

