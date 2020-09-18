---
UID: NF:strmif.IFilterGraph.RemoveFilter
title: IFilterGraph::RemoveFilter (strmif.h)
description: The RemoveFilter method removes a filter from the graph.
helpviewer_keywords: ["IFilterGraph interface [DirectShow]","RemoveFilter method","IFilterGraph.RemoveFilter","IFilterGraph::RemoveFilter","IFilterGraphRemoveFilter","RemoveFilter","RemoveFilter method [DirectShow]","RemoveFilter method [DirectShow]","IFilterGraph interface","dshow.ifiltergraph_removefilter","strmif/IFilterGraph::RemoveFilter"]
old-location: dshow\ifiltergraph_removefilter.htm
tech.root: dshow
ms.assetid: ec681340-0fb9-4eba-8211-d5fa07fb076b
ms.date: 12/05/2018
ms.keywords: IFilterGraph interface [DirectShow],RemoveFilter method, IFilterGraph.RemoveFilter, IFilterGraph::RemoveFilter, IFilterGraphRemoveFilter, RemoveFilter, RemoveFilter method [DirectShow], RemoveFilter method [DirectShow],IFilterGraph interface, dshow.ifiltergraph_removefilter, strmif/IFilterGraph::RemoveFilter
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
 - IFilterGraph::RemoveFilter
 - strmif/IFilterGraph::RemoveFilter
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
 - IFilterGraph.RemoveFilter
---

# IFilterGraph::RemoveFilter


## -description

The <code>RemoveFilter</code> method removes a filter from the graph.

## -parameters

### -param pFilter [in]

Pointer to the filter to be removed from the graph.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

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

## -remarks

The Filter Graph Manager notifies the filter that it is being removed by calling the filter's <a href="/windows/desktop/api/strmif/nf-strmif-ibasefilter-joinfiltergraph">IBaseFilter::JoinFilterGraph</a> method with a <b>NULL</b> argument. It is not necessary to disconnect the filter's pins before calling <code>RemoveFilter</code>, but the filter graph should be in the Stopped state. If the filters are not stopped, <code>RemoveFilter</code> may fail to disconnect the pins and then fail to remove the filter from the graph. <a href="/windows/desktop/api/strmif/nf-strmif-igraphconfig-removefilterex">IGraphConfig::RemoveFilterEx</a> enables an application to remove a filter without disconnecting the pins automatically, which improves performance if you want to move groups of connected filters into a new graph.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ifiltergraph">IFilterGraph Interface</a>