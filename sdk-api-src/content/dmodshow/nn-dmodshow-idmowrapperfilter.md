---
UID: NN:dmodshow.IDMOWrapperFilter
title: IDMOWrapperFilter (dmodshow.h)
description: The IDMOWrapperFilter interface enables an application to use a DirectX Media Object (DMO) inside a filter graph.
helpviewer_keywords: ["IDMOWrapperFilter","IDMOWrapperFilter interface [DirectShow]","IDMOWrapperFilter interface [DirectShow]","described","IDMOWrapperFilterInterface","dmodshow/IDMOWrapperFilter","dshow.idmowrapperfilter"]
old-location: dshow\idmowrapperfilter.htm
tech.root: dshow
ms.assetid: c85b828c-095d-4991-85a8-65b96529f305
ms.date: 12/05/2018
ms.keywords: IDMOWrapperFilter, IDMOWrapperFilter interface [DirectShow], IDMOWrapperFilter interface [DirectShow],described, IDMOWrapperFilterInterface, dmodshow/IDMOWrapperFilter, dshow.idmowrapperfilter
f1_keywords:
- dmodshow/IDMOWrapperFilter
dev_langs:
- c++
req.header: dmodshow.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Dmoguids.lib
- Dmoguids.dll
api_name:
- IDMOWrapperFilter
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDMOWrapperFilter interface


## -description



The <code>IDMOWrapperFilter</code> interface enables an application to use a DirectX Media Object (DMO) inside a filter graph. The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/dmo-wrapper-filter">DMO Wrapper</a> filter exposes this interface.

To add a DMO to the filter graph, create an instance of the DMO Wrapper filter and query it for the <code>IDMOWrapperFilter</code> interface. Then call the <a href="https://docs.microsoft.com/windows/desktop/api/dmodshow/nf-dmodshow-idmowrapperfilter-init">IDMOWrapperFilter::Init</a> method to initialize the filter with the DMO.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDMOWrapperFilter</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDMOWrapperFilter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDMOWrapperFilter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dmodshow/nf-dmodshow-idmowrapperfilter-init">Init</a>
</td>
<td align="left" width="63%">
Initializes the DMO Wrapper filter with the specified DMO.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/directx-media-objects">DirectX Media Objects</a>
 

 

