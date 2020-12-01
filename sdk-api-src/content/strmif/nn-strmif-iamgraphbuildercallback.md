---
UID: NN:strmif.IAMGraphBuilderCallback
title: IAMGraphBuilderCallback (strmif.h)
description: The IAMGraphBuilderCallback interface provides a callback mechanism during graph building.To use this interface, implement the interface in your application or client object.
helpviewer_keywords: ["IAMGraphBuilderCallback","IAMGraphBuilderCallback interface [DirectShow]","IAMGraphBuilderCallback interface [DirectShow]","described","IAMGraphBuilderCallbackInterface","dshow.iamgraphbuildercallback","strmif/IAMGraphBuilderCallback"]
old-location: dshow\iamgraphbuildercallback.htm
tech.root: dshow
ms.assetid: 4d8e45e3-7144-44ad-b79e-5acc0cec6ed4
ms.date: 12/05/2018
ms.keywords: IAMGraphBuilderCallback, IAMGraphBuilderCallback interface [DirectShow], IAMGraphBuilderCallback interface [DirectShow],described, IAMGraphBuilderCallbackInterface, dshow.iamgraphbuildercallback, strmif/IAMGraphBuilderCallback
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
 - IAMGraphBuilderCallback
 - strmif/IAMGraphBuilderCallback
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
 - IAMGraphBuilderCallback
---

# IAMGraphBuilderCallback interface


## -description

The <code>IAMGraphBuilderCallback</code> interface provides a callback mechanism during graph building.

To use this interface, implement the interface in your application or client object. Query the Filter Graph Manager for the <b>IObjectWithSite</b> interface and call the <b>IObjectWithSite::SetSite</b> method with a pointer to your implementation of the interface. The Filter Graph Manager calls the methods on this interface while it builds the graph, which gives the client the opportunity to modify the graph-building process.

The primary use for this interface is to configure the Video Mixing Renderer filter before it is connected. You can also use it reject a specific filter during graph building, such as a decoder filter.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMGraphBuilderCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMGraphBuilderCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMGraphBuilderCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/strmif/nf-strmif-iamgraphbuildercallback-createdfilter">CreatedFilter</a>
</td>
<td align="left" width="63%">
Called after the Filter Graph Manager creates a filter, but before it tries to connect the filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/strmif/nf-strmif-iamgraphbuildercallback-selectedfilter">SelectedFilter</a>
</td>
<td align="left" width="63%">
Called when the Filter Graph Manager finds a candidate filter, but before it creates the filter.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-iamfiltergraphcallback">IAMFilterGraphCallback Interface</a>