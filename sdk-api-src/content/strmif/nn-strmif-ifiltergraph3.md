---
UID: NN:strmif.IFilterGraph3
title: IFilterGraph3 (strmif.h)
description: The IFilterGraph3 interface extends the IFilterGraph2 interface, which contains methods for building filter graphs.The Filter Graph Manager implements this interface.
helpviewer_keywords: ["IFilterGraph3","IFilterGraph3 interface [DirectShow]","IFilterGraph3 interface [DirectShow]","described","IFilterGraph3Interface","dshow.ifiltergraph3","strmif/IFilterGraph3"]
old-location: dshow\ifiltergraph3.htm
tech.root: dshow
ms.assetid: 1d5f8eda-2b09-4627-8ae9-f43f38c3c26a
ms.date: 12/05/2018
ms.keywords: IFilterGraph3, IFilterGraph3 interface [DirectShow], IFilterGraph3 interface [DirectShow],described, IFilterGraph3Interface, dshow.ifiltergraph3, strmif/IFilterGraph3
f1_keywords:
- strmif/IFilterGraph3
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
- IFilterGraph3
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFilterGraph3 interface


## -description



The <code>IFilterGraph3</code> interface extends the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ifiltergraph2">IFilterGraph2</a> interface, which contains methods for building filter graphs.

The Filter Graph Manager implements this interface. Applications can use it when building graphs, to take advantage of the additional methods it provides.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFilterGraph3</b> interface inherits from <b>IFilterGraph2</b>. <b>IFilterGraph3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFilterGraph3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ifiltergraph3-setsyncsourceex">SetSyncSourceEx</a>
</td>
<td align="left" width="63%">
Sets a primary and secondary reference clock for the filter graph.

</td>
</tr>
</table> 

