---
UID: NN:strmif.ICaptureGraphBuilder2
title: ICaptureGraphBuilder2 (strmif.h)
description: The ICaptureGraphBuilder2 interface builds capture graphs and other custom filter graphs.
old-location: dshow\icapturegraphbuilder2.htm
tech.root: DirectShow
ms.assetid: abdf6fb2-e98f-4df8-98ec-06d33798abb5
ms.date: 12/05/2018
ms.keywords: ICaptureGraphBuilder2, ICaptureGraphBuilder2 interface [DirectShow], ICaptureGraphBuilder2 interface [DirectShow],described, ICaptureGraphBuilder2Interface, dshow.icapturegraphbuilder2, strmif/ICaptureGraphBuilder2
f1_keywords:
- strmif/ICaptureGraphBuilder2
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
- ICaptureGraphBuilder2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICaptureGraphBuilder2 interface


## -description



The <code>ICaptureGraphBuilder2</code> interface builds capture graphs and other custom filter graphs. The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/capture-graph-builder">Capture Graph Builder</a> object implements this interface.

<div class="alert"><b>Note</b>  By default, the <code>ICaptureGraphBuilder2</code> interface does not use the Video Mixing Renderer (VMR), Enhanced Video Renderer (EVR) or <a href="https://docs.microsoft.com/windows/desktop/DirectShow/video-port-manager">Video Port Manager</a> filters.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICaptureGraphBuilder2</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICaptureGraphBuilder2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICaptureGraphBuilder2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-icapturegraphbuilder2-alloccapfile">AllocCapFile</a>
</td>
<td align="left" width="63%">
Preallocates a capture file to a specified size.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-icapturegraphbuilder2-controlstream">ControlStream</a>
</td>
<td align="left" width="63%">
Sets the start and stop times for one or more streams of captured data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-icapturegraphbuilder2-copycapturefile">CopyCaptureFile</a>
</td>
<td align="left" width="63%">
Copies the valid media data from a capture file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-icapturegraphbuilder2-findinterface">FindInterface</a>
</td>
<td align="left" width="63%">
Searches the graph for a specified interface, starting from a specified filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-icapturegraphbuilder2-findpin">FindPin</a>
</td>
<td align="left" width="63%">
Retrieves a particular pin on a filter, or determines whether a given pin matches the specified criteria.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-icapturegraphbuilder2-getfiltergraph">GetFiltergraph</a>
</td>
<td align="left" width="63%">
Retrieves the filter graph that the builder is using.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-icapturegraphbuilder2-renderstream">RenderStream</a>
</td>
<td align="left" width="63%">
Connects an output pin on a source filter to a rendering filter, optionally through a compression filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph">SetFiltergraph</a>
</td>
<td align="left" width="63%">
Specifies a filter graph for the capture graph builder to use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename">SetOutputFileName</a>
</td>
<td align="left" width="63%">
Creates the file writing section of the filter graph.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/building-graphs-with-the-capture-graph-builder">Building Graphs with the Capture Graph Builder</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/recompressing-an-avi-file">Recompressing an AVI File</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/video-capture">Video Capture</a>
 

 

