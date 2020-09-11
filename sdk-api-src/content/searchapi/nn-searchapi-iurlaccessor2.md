---
UID: NN:searchapi.IUrlAccessor2
title: IUrlAccessor2 (searchapi.h)
description: Extends functionality of the IUrlAccessor interface.
helpviewer_keywords: ["IUrlAccessor2","IUrlAccessor2 interface [search]","IUrlAccessor2 interface [search]","described","_search_IUrlAccessor2","search._search_IUrlAccessor2","searchapi/IUrlAccessor2"]
old-location: search\_search_IUrlAccessor2.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\iurlaccessor2\iurlaccessor2.htm
ms.date: 12/05/2018
ms.keywords: IUrlAccessor2, IUrlAccessor2 interface [search], IUrlAccessor2 interface [search],described, _search_IUrlAccessor2, search._search_IUrlAccessor2, searchapi/IUrlAccessor2
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Urlaccsdk.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - IUrlAccessor2
 - searchapi/IUrlAccessor2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Searchapi.h
api_name:
 - IUrlAccessor2
---

# IUrlAccessor2 interface


## -description

Extends functionality of the <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor">IUrlAccessor</a> interface.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUrlAccessor2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor">IUrlAccessor</a>. <b>IUrlAccessor2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUrlAccessor2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-iurlaccessor2-getcodepage">GetCodePage</a>
</td>
<td align="left" width="63%">
Gets the code page for properties of the URL item.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-iurlaccessor2-getdisplayurl">GetDisplayUrl</a>
</td>
<td align="left" width="63%">
Gets the user-friendly path for the URL item.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-iurlaccessor2-isdocument">IsDocument</a>
</td>
<td align="left" width="63%">
Ascertains whether an item URL is a document or directory.

</td>
</tr>
</table>

## -see-also

<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor">IUrlAccessor</a>



<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor3">IUrlAccessor3</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/search/-search-prth-error-constants">Search Protocol Handler Error Messages</a>



<a href="https://docs.microsoft.com/windows/desktop/search/-search-indexing-process-overview">The Indexing Process</a>

