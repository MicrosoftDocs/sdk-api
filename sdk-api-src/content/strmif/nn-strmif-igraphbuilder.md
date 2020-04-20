---
UID: NN:strmif.IGraphBuilder
title: IGraphBuilder (strmif.h)
description: This interface provides methods that enable an application to build a filter graph.helpviewer_keywords: ["IGraphBuilder","IGraphBuilder interface [DirectShow]","IGraphBuilder interface [DirectShow]","described","IGraphBuilderInterface","dshow.igraphbuilder","strmif/IGraphBuilder"]
old-location: dshow\igraphbuilder.htm
tech.root: DirectShow
ms.assetid: 54ed8ac8-4821-4c0c-9fb9-789c70dbca37
ms.date: 12/05/2018
ms.keywords: IGraphBuilder, IGraphBuilder interface [DirectShow], IGraphBuilder interface [DirectShow],described, IGraphBuilderInterface, dshow.igraphbuilder, strmif/IGraphBuilder
f1_keywords:
- strmif/IGraphBuilder
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
- IGraphBuilder
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGraphBuilder interface


## -description



This interface provides methods that enable an application to build a filter graph. The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/filter-graph-manager">Filter Graph Manager</a> implements this interface.

The <b>IGraphBuilder</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ifiltergraph">IFilterGraph</a> interface. <b>IFilterGraph</b> provides basic operations, such as adding a filter to the graph or connecting two pins. <b>IGraphBuilder</b> adds further methods that construct graphs from partial information. For example, the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-igraphbuilder-renderfile">IGraphBuilder::RenderFile</a> method builds a graph for file playback, given the name of the file. The <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-igraphbuilder-render">IGraphBuilder::Render</a> method renders data from an output pin by connecting new filters to the pin.

Using these methods, an application does not need to specify every filter and pin connection in the graph. Instead, the Filter Graph Manager selects filters that are registered on the user's system, adds them to the graph, and connects them. For more information, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/intelligent-connect">Intelligent Connect</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGraphBuilder</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ifiltergraph">IFilterGraph</a>. <b>IGraphBuilder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IGraphBuilder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-igraphbuilder-abort">Abort</a>
</td>
<td align="left" width="63%">
Requests that the graph builder return as soon as possible from its current task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-igraphbuilder-addsourcefilter">AddSourceFilter</a>
</td>
<td align="left" width="63%">
Adds a source filter to the filter graph for a specific file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-igraphbuilder-connect">Connect</a>
</td>
<td align="left" width="63%">
Connects two pins. If they will not connect directly, this method connects them with intervening transforms.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-igraphbuilder-render">Render</a>
</td>
<td align="left" width="63%">
Adds a chain of filters to a specified output pin to render it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-igraphbuilder-renderfile">RenderFile</a>
</td>
<td align="left" width="63%">
Builds a filter graph that renders the specified file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-igraphbuilder-setlogfile">SetLogFile</a>
</td>
<td align="left" width="63%">
Sets the file for logging actions taken when attempting to perform an operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-igraphbuilder-shouldoperationcontinue">ShouldOperationContinue</a>
</td>
<td align="left" width="63%">
Queries whether the current operation should continue.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ifiltergraph">IFilterGraph</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/interfaces">Interfaces</a>
 

 

