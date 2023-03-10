---
UID: NF:strmif.IDistributorNotify.NotifyGraphChange
title: IDistributorNotify::NotifyGraphChange (strmif.h)
description: The NotifyGraphChange method is called when the set of filters in the filter graph changes or any pin connections change.
helpviewer_keywords: ["IDistributorNotify interface [DirectShow]","NotifyGraphChange method","IDistributorNotify.NotifyGraphChange","IDistributorNotify::NotifyGraphChange","IDistributorNotifyNotifyGraphChange","NotifyGraphChange","NotifyGraphChange method [DirectShow]","NotifyGraphChange method [DirectShow]","IDistributorNotify interface","dshow.idistributornotify_notifygraphchange","strmif/IDistributorNotify::NotifyGraphChange"]
old-location: dshow\idistributornotify_notifygraphchange.htm
tech.root: dshow
ms.assetid: 5f77f674-643a-450a-9589-16866d6cf680
ms.date: 12/05/2018
ms.keywords: IDistributorNotify interface [DirectShow],NotifyGraphChange method, IDistributorNotify.NotifyGraphChange, IDistributorNotify::NotifyGraphChange, IDistributorNotifyNotifyGraphChange, NotifyGraphChange, NotifyGraphChange method [DirectShow], NotifyGraphChange method [DirectShow],IDistributorNotify interface, dshow.idistributornotify_notifygraphchange, strmif/IDistributorNotify::NotifyGraphChange
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
 - IDistributorNotify::NotifyGraphChange
 - strmif/IDistributorNotify::NotifyGraphChange
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
 - IDistributorNotify.NotifyGraphChange
---

# IDistributorNotify::NotifyGraphChange


## -description

The <code>NotifyGraphChange</code> method is called when the set of filters in the filter graph changes or any pin connections change.



## -returns

Returns an <b>HRESULT</b> value.

## -remarks

This method is called whenever the <a href="/windows/desktop/api/strmif/nf-strmif-ifiltergraph-addfilter">IFilterGraph::AddFilter</a>, <a href="/windows/desktop/api/strmif/nf-strmif-ifiltergraph-removefilter">IFilterGraph::RemoveFilter</a>, or <a href="/windows/desktop/api/strmif/nf-strmif-ifiltergraph-connectdirect">IFilterGraph::ConnectDirect</a> method is called or a method is called that will lead to one of these being called (such as <a href="/windows/desktop/api/strmif/nf-strmif-igraphbuilder-renderfile">IGraphBuilder::RenderFile</a>).

Make sure you call <b>Release</b> on any held filters that have been removed at this point. For performance reasons, PIDs might choose not to rescan the filters until the PIDs actually need the interfaces, because there might be several separate notifications sent. However, it is important to release any cached interfaces immediately.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idistributornotify">IDistributorNotify Interface</a>
