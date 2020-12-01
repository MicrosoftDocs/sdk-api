---
UID: NF:strmif.IDvdGraphBuilder.GetFiltergraph
title: IDvdGraphBuilder::GetFiltergraph (strmif.h)
description: The GetFiltergraph method retrieves the IGraphBuilder interface for the filter graph used by the DVD-Video graph builder object.
helpviewer_keywords: ["GetFiltergraph","GetFiltergraph method [DirectShow]","GetFiltergraph method [DirectShow]","IDvdGraphBuilder interface","IDvdGraphBuilder interface [DirectShow]","GetFiltergraph method","IDvdGraphBuilder.GetFiltergraph","IDvdGraphBuilder::GetFiltergraph","IDvdGraphBuilderGetFiltergraph","dshow.idvdgraphbuilder_getfiltergraph","strmif/IDvdGraphBuilder::GetFiltergraph"]
old-location: dshow\idvdgraphbuilder_getfiltergraph.htm
tech.root: dshow
ms.assetid: 1f12140b-d10d-47d9-8bac-33fab084bff4
ms.date: 12/05/2018
ms.keywords: GetFiltergraph, GetFiltergraph method [DirectShow], GetFiltergraph method [DirectShow],IDvdGraphBuilder interface, IDvdGraphBuilder interface [DirectShow],GetFiltergraph method, IDvdGraphBuilder.GetFiltergraph, IDvdGraphBuilder::GetFiltergraph, IDvdGraphBuilderGetFiltergraph, dshow.idvdgraphbuilder_getfiltergraph, strmif/IDvdGraphBuilder::GetFiltergraph
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
 - IDvdGraphBuilder::GetFiltergraph
 - strmif/IDvdGraphBuilder::GetFiltergraph
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
 - IDvdGraphBuilder.GetFiltergraph
---

# IDvdGraphBuilder::GetFiltergraph


## -description

The <code>GetFiltergraph</code> method retrieves the <a href="/windows/desktop/api/strmif/nn-strmif-igraphbuilder">IGraphBuilder</a> interface for the filter graph used by the DVD-Video graph builder object.

## -parameters

### -param ppGB [out]

Address of a pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-igraphbuilder">IGraphBuilder</a> interface that the DVD-Video graph builder object is using.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface. The current DirectShow implementation returns E_INVALIDARG if <i>ppGB</i> is invalid.

## -remarks

The returned <b>IGraphBuilder</b> interface pointer has an outstanding reference count. The caller must release the interface.

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdgraphbuilder">IDvdGraphBuilder Interface</a>