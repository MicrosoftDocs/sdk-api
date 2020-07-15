---
UID: NN:strmif.IDvdGraphBuilder
title: IDvdGraphBuilder (strmif.h)
description: The IDvdGraphBuilder interface builds a filter graph for DVD-Video playback.
helpviewer_keywords: ["IDvdGraphBuilder","IDvdGraphBuilder interface [DirectShow]","IDvdGraphBuilder interface [DirectShow]","described","IDvdGraphBuilderInterface","dshow.idvdgraphbuilder","strmif/IDvdGraphBuilder"]
old-location: dshow\idvdgraphbuilder.htm
tech.root: DirectShow
ms.assetid: 2179e54a-c6e2-4837-9f89-be210bde9180
ms.date: 12/05/2018
ms.keywords: IDvdGraphBuilder, IDvdGraphBuilder interface [DirectShow], IDvdGraphBuilder interface [DirectShow],described, IDvdGraphBuilderInterface, dshow.idvdgraphbuilder, strmif/IDvdGraphBuilder
f1_keywords:
- strmif/IDvdGraphBuilder
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
- IDvdGraphBuilder
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdGraphBuilder interface


## -description



The <code>IDvdGraphBuilder</code> interface builds a filter graph for DVD-Video playback. The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-graph-builder">DVD Graph Builder</a> object implements this interface.

The <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume">RenderDvdVideoVolume</a> method builds a DVD playback graph from the available software and hardware on the system. For information on how to build the DVD filter graph and obtain the pointers to all the necessary interfaces, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/building-the-dvd-filter-graph">Building the DVD Filter Graph</a>.

<div class="alert"><b>Note</b>  A DVD filter graph requires either a hardware or software MPEG-2 decoder.</div>
<div> </div>
Generally, you should not add, remove, connect, disconnect, or access individual filters in the graph created by <b>RenderDvdVideoVolume</b>, because doing so might confuse the cleanup code. The purpose of the <b>DvdGraphBuilder</b> object is to simplify the development of DVD-Video applications. If you need a specific type of graph for a particular solution, you should manually create the entire filter graph.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvdGraphBuilder</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDvdGraphBuilder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvdGraphBuilder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdgraphbuilder-getdvdinterface">GetDvdInterface</a>
</td>
<td align="left" width="63%">
Retrieves interfaces from the DVD-Video playback graph to make DVD-Video playback development easier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdgraphbuilder-getfiltergraph">GetFiltergraph</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-igraphbuilder">IGraphBuilder</a> interface for the filter graph used by the DVD-Video graph builder object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume">RenderDvdVideoVolume</a>
</td>
<td align="left" width="63%">
Completes building a filter graph according to user specifications for playing a DVD-Video volume.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>
 

 

