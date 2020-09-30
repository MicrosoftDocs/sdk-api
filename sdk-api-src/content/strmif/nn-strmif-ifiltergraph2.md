---
UID: NN:strmif.IFilterGraph2
title: IFilterGraph2 (strmif.h)
description: The IFilterGraph2 interface extends the IFilterGraph and IGraphBuilder interfaces, which contain methods for building filter graphs.The Filter Graph Manager implements this interface.
helpviewer_keywords: ["IFilterGraph2","IFilterGraph2 interface [DirectShow]","IFilterGraph2 interface [DirectShow]","described","IFilterGraph2Interface","dshow.ifiltergraph2","strmif/IFilterGraph2"]
old-location: dshow\ifiltergraph2.htm
tech.root: dshow
ms.assetid: 1a1ef4fe-a054-4ba7-99c7-1f209472c5a6
ms.date: 12/05/2018
ms.keywords: IFilterGraph2, IFilterGraph2 interface [DirectShow], IFilterGraph2 interface [DirectShow],described, IFilterGraph2Interface, dshow.ifiltergraph2, strmif/IFilterGraph2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFilterGraph2
 - strmif/IFilterGraph2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IFilterGraph2
---

# IFilterGraph2 interface


## -description

The <code>IFilterGraph2</code> interface extends the <a href="/windows/desktop/api/strmif/nn-strmif-ifiltergraph">IFilterGraph</a> and <a href="/windows/desktop/api/strmif/nn-strmif-igraphbuilder">IGraphBuilder</a> interfaces, which contain methods for building filter graphs.

The Filter Graph Manager implements this interface. Applications can use it when building graphs, to take advantage of the additional methods it provides.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFilterGraph2</b> interface inherits from <a href="/windows/desktop/api/strmif/nn-strmif-igraphbuilder">IGraphBuilder</a>. <b>IFilterGraph2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFilterGraph2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/strmif/nf-strmif-ifiltergraph2-addsourcefilterformoniker">AddSourceFilterForMoniker</a>
</td>
<td align="left" width="63%">
Creates a source filter from a moniker and adds it to the graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/strmif/nf-strmif-ifiltergraph2-reconnectex">ReconnectEx</a>
</td>
<td align="left" width="63%">
Breaks an existing pin connection and reconnects the same pins, using a specified media type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/strmif/nf-strmif-ifiltergraph2-renderex">RenderEx</a>
</td>
<td align="left" width="63%">
Renders an output pin, with an option to use existing renderers only.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-igraphbuilder">IGraphBuilder</a>