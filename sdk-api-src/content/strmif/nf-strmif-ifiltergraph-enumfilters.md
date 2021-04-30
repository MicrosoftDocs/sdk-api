---
UID: NF:strmif.IFilterGraph.EnumFilters
title: IFilterGraph::EnumFilters (strmif.h)
description: The EnumFilters method provides an enumerator for all filters in the graph.
helpviewer_keywords: ["EnumFilters","EnumFilters method [DirectShow]","EnumFilters method [DirectShow]","IFilterGraph interface","EnumFilters method [DirectShow]","IGraphBuilder interface","IFilterGraph interface [DirectShow]","EnumFilters method","IFilterGraph.EnumFilters","IFilterGraph::EnumFilters","IFilterGraphEnumFilters","IGraphBuilder interface [DirectShow]","EnumFilters method","IGraphBuilder.EnumFilters","IGraphBuilder::EnumFilters","dshow.ifiltergraph_enumfilters","strmif/IFilterGraph::EnumFilters","strmif/IGraphBuilder::EnumFilters"]
old-location: dshow\ifiltergraph_enumfilters.htm
tech.root: dshow
ms.assetid: 3a6dcd1a-3ec3-4f0f-8e82-2d33ad775eec
ms.date: 12/05/2018
ms.keywords: EnumFilters, EnumFilters method [DirectShow], EnumFilters method [DirectShow],IFilterGraph interface, EnumFilters method [DirectShow],IGraphBuilder interface, IFilterGraph interface [DirectShow],EnumFilters method, IFilterGraph.EnumFilters, IFilterGraph::EnumFilters, IFilterGraphEnumFilters, IGraphBuilder interface [DirectShow],EnumFilters method, IGraphBuilder.EnumFilters, IGraphBuilder::EnumFilters, dshow.ifiltergraph_enumfilters, strmif/IFilterGraph::EnumFilters, strmif/IGraphBuilder::EnumFilters
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
 - IFilterGraph::EnumFilters
 - strmif/IFilterGraph::EnumFilters
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
 - IFilterGraph.EnumFilters
 - IGraphBuilder.EnumFilters
 - IGraphBuilder.EnumFilters
---

# IFilterGraph::EnumFilters


## -description

The <code>EnumFilters</code> method provides an enumerator for all filters in the graph.

## -parameters

### -param ppEnum [out]

Receives a pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-ienumfilters">IEnumFilters</a> interface. Use this interface to enumerate the filters. The caller must release the interface.

## -returns

Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to create the enumerator.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ifiltergraph">IFilterGraph Interface</a>