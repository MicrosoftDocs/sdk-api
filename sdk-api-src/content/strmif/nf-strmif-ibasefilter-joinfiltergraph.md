---
UID: NF:strmif.IBaseFilter.JoinFilterGraph
title: IBaseFilter::JoinFilterGraph (strmif.h)
description: The JoinFilterGraph method notifies the filter that it has joined or left the filter graph.helpviewer_keywords: ["IBaseFilter interface [DirectShow]","JoinFilterGraph method","IBaseFilter.JoinFilterGraph","IBaseFilter::JoinFilterGraph","IBaseFilterJoinFilterGraph","JoinFilterGraph","JoinFilterGraph method [DirectShow]","JoinFilterGraph method [DirectShow]","IBaseFilter interface","dshow.ibasefilter_joinfiltergraph","strmif/IBaseFilter::JoinFilterGraph"]
old-location: dshow\ibasefilter_joinfiltergraph.htm
tech.root: DirectShow
ms.assetid: 1f01c71f-5c12-4bf3-937c-740168baf776
ms.date: 12/05/2018
ms.keywords: IBaseFilter interface [DirectShow],JoinFilterGraph method, IBaseFilter.JoinFilterGraph, IBaseFilter::JoinFilterGraph, IBaseFilterJoinFilterGraph, JoinFilterGraph, JoinFilterGraph method [DirectShow], JoinFilterGraph method [DirectShow],IBaseFilter interface, dshow.ibasefilter_joinfiltergraph, strmif/IBaseFilter::JoinFilterGraph
f1_keywords:
- strmif/IBaseFilter.JoinFilterGraph
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
- IBaseFilter.JoinFilterGraph
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBaseFilter::JoinFilterGraph


## -description



The <code>JoinFilterGraph</code> method notifies the filter that it has joined or left the filter graph.




## -parameters




### -param pGraph [in]

Pointer to the Filter Graph Manager's <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ifiltergraph">IFilterGraph</a> interface, or <b>NULL</b> if the filter is leaving the graph.


### -param pName [in]

Pointer to a wide-character string that specifies a name for the filter.


## -returns



Returns S_OK if successful, or an <b>HRESULT</b> value indicating the cause of the error.




## -remarks



When the Filter Graph Manager adds a filter to the filter graph, it calls this method with a pointer to itself. It assigns a name for this instance of the filter through the <i>pName</i> parameter. The name can be retrieved by calling the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ibasefilter-queryfilterinfo">IBaseFilter::QueryFilterInfo</a> method.

When the Filter Graph Manager removes the filter from the graph, it calls this method with a <b>NULL</b> pointer.

Applications should never call this method. To add a filter to the graph, call the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ifiltergraph-addfilter">IFilterGraph::AddFilter</a> method on the filter graph manager.

<b>Filter developers</b>: The filter can store the <b>IFilterGraph</b> interface pointer and query it for other Filter Graph Manager interfaces. However, it must never hold a reference count on the Filter Graph Manager. Doing so creates a circular reference count, because the Filter Graph Manager keeps a reference count on the filter. A circular reference count prevents the interface from being released properly, which can lead to a deadlock. The <b>IFilterGraph</b> interface is guaranteed to be valid until the Filter Graph Manager calls this method again with the value <b>NULL</b>. For an implementation of this method, see the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/cbasefilter-joinfiltergraph">CBaseFilter::JoinFilterGraph</a> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter Interface</a>
 

 

