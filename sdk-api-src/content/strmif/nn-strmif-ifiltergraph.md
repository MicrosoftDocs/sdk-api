---
UID: NN:strmif.IFilterGraph
title: IFilterGraph (strmif.h)
author: windows-sdk-content
description: The IFilterGraph interface provides methods for building a filter graph.
old-location: dshow\ifiltergraph.htm
tech.root: DirectShow
ms.assetid: 73a92f44-03c6-47e3-98d1-a20100ed8fa1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFilterGraph, IFilterGraph interface [DirectShow], IFilterGraph interface [DirectShow],described, IFilterGraphInterface, dshow.ifiltergraph, strmif/IFilterGraph
ms.topic: interface
f1_keywords: 
 - "strmif/IFilterGraph"
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
 - IFilterGraph
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFilterGraph interface


## -description



The <code>IFilterGraph</code> interface provides methods for building a filter graph. An application can use it to add filters to the graph, connect or disconnect filters, remove filters, and perform other basic operations. However, the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-igraphbuilder">IGraphBuilder</a> interface inherits from this interface and provides additional methods that are more sophisticated. Therefore, applications should use <b>IGraphBuilder</b> rather than using <code>IFilterGraph</code> directly.

The filter graph manager implements this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFilterGraph</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFilterGraph</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFilterGraph</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ifiltergraph-addfilter">AddFilter</a>
</td>
<td align="left" width="63%">
Adds a filter to the graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ifiltergraph-connectdirect">ConnectDirect</a>
</td>
<td align="left" width="63%">
Connects two pins directly (without intervening filters).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ifiltergraph-disconnect">Disconnect</a>
</td>
<td align="left" width="63%">
Disconnects a specified pin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ifiltergraph-enumfilters">EnumFilters</a>
</td>
<td align="left" width="63%">
Provides an enumerator for all filters in the graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ifiltergraph-findfilterbyname">FindFilterByName</a>
</td>
<td align="left" width="63%">
Finds a filter that was added with a specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ifiltergraph-reconnect">Reconnect</a>
</td>
<td align="left" width="63%">
Breaks the existing pin connection and reconnects it to the same pin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ifiltergraph-removefilter">RemoveFilter</a>
</td>
<td align="left" width="63%">
Removes a filter from the graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ifiltergraph-setdefaultsyncsource">SetDefaultSyncSource</a>
</td>
<td align="left" width="63%">
Sets the reference clock to the default clock.

</td>
</tr>
</table> 

