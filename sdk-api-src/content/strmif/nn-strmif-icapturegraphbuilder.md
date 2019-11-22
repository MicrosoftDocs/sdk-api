---
UID: NN:strmif.ICaptureGraphBuilder
title: ICaptureGraphBuilder (strmif.h)

description: Note  This interface has been deprecated.
old-location: dshow\icapturegraphbuilder.htm
tech.root: DirectShow
ms.assetid: 64ee80cd-9f63-4f38-853a-1ecfc03e6076

ms.date: 12/05/2018
ms.keywords: ICaptureGraphBuilder, ICaptureGraphBuilder interface [DirectShow], ICaptureGraphBuilder interface [DirectShow],described, ICaptureGraphBuilderInterface, dshow.icapturegraphbuilder, strmif/ICaptureGraphBuilder
ms.topic: interface
f1_keywords: 
 - "strmif/ICaptureGraphBuilder"
dev_langs:
 - c++
req.header: strmif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmif.h
api_name:
 - ICaptureGraphBuilder
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICaptureGraphBuilder interface


## -description



<div class="alert"><b>Note</b>  This interface has been deprecated. It will continue to be supported for backward compatibility with existing applications, but new applications should use the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-icapturegraphbuilder2">ICaptureGraphBuilder2</a> interface.</div>
<div> </div>
The <code>ICaptureGraphBuilder</code> interface enables you to build capture graphs, preview graphs, file recompression graphs, or other custom graphs.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICaptureGraphBuilder</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICaptureGraphBuilder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICaptureGraphBuilder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-icapturegraphbuilder-alloccapfile">AllocCapFile</a>
</td>
<td align="left" width="63%">
Preallocates a capture file to a specified size.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-icapturegraphbuilder-controlstream">ControlStream</a>
</td>
<td align="left" width="63%">
Sends stream control messages to the pin of the specified category on one or more capture filters in a graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-icapturegraphbuilder-copycapturefile">CopyCaptureFile</a>
</td>
<td align="left" width="63%">
Copies the valid media data from the preallocated capture file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-icapturegraphbuilder-findinterface">FindInterface</a>
</td>
<td align="left" width="63%">
Looks for the specified interface on the filter, upstream and downstream from the filter, and, optionally, only on the output pin of the given category.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-icapturegraphbuilder-getfiltergraph">GetFiltergraph</a>
</td>
<td align="left" width="63%">
Retrieves the filter graph that the builder is using.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-icapturegraphbuilder-renderstream">RenderStream</a>
</td>
<td align="left" width="63%">
Connects a source filter's pin, of an optionally specified category, to the rendering filter, and optionally through another filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-icapturegraphbuilder-setfiltergraph">SetFiltergraph</a>
</td>
<td align="left" width="63%">
Tells the graph builder object which filter graph to use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-icapturegraphbuilder-setoutputfilename">SetOutputFileName</a>
</td>
<td align="left" width="63%">
Creates the rendering section of the filter graph, which will save bits to disk with the specified file name.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/deprecated-interfaces">Deprecated Interfaces</a>
 

 

