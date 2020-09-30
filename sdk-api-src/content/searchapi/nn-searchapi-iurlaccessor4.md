---
UID: NN:searchapi.IUrlAccessor4
title: IUrlAccessor4 (searchapi.h)
description: Extends the functionality of the IUrlAccessor3 interface with the IUrlAccessor4::ShouldIndexItemContent method that identifies whether the content of the item should be indexed.
helpviewer_keywords: ["IUrlAccessor4","IUrlAccessor4 interface [search]","IUrlAccessor4 interface [search]","described","_search_IUrlAccessor4","search._search_IUrlAccessor4","searchapi/IUrlAccessor4"]
old-location: search\_search_IUrlAccessor4.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\protocolhandlers\iurlaccessor4\iurlaccessor4.htm
ms.date: 12/05/2018
ms.keywords: IUrlAccessor4, IUrlAccessor4 interface [search], IUrlAccessor4 interface [search],described, _search_IUrlAccessor4, search._search_IUrlAccessor4, searchapi/IUrlAccessor4
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.redist: Windows Search (WS) 4.0
ms.custom: 19H1
f1_keywords:
 - IUrlAccessor4
 - searchapi/IUrlAccessor4
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
 - IUrlAccessor4
---

# IUrlAccessor4 interface


## -description

Extends the functionality of the <a href="/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor3">IUrlAccessor3</a> interface with the <a href="/windows/desktop/api/searchapi/nf-searchapi-iurlaccessor4-shouldindexitemcontent">IUrlAccessor4::ShouldIndexItemContent</a> method that identifies whether the content of the item should be indexed.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUrlAccessor4</b> interface inherits from <a href="/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor3">IUrlAccessor3</a>. <b>IUrlAccessor4</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUrlAccessor4</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/searchapi/nf-searchapi-iurlaccessor2-getcodepage">GetCodePage</a>
</td>
<td align="left" width="63%">
Gets the code page for properties of the URL item.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/searchapi/nf-searchapi-iurlaccessor2-getdisplayurl">GetDisplayUrl</a>
</td>
<td align="left" width="63%">
Gets the user-friendly path for the URL item.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/searchapi/nf-searchapi-iurlaccessor3-getimpersonationsidblobs">GetImpersonationSidBlobs</a>
</td>
<td align="left" width="63%">
Retrieves an array of user SIDs for a specified URL. This method enables protocol handlers to specify which users can access the file and the search protocol host to impersonate a user in order to index the file.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/searchapi/nf-searchapi-iurlaccessor2-isdocument">IsDocument</a>
</td>
<td align="left" width="63%">
Ascertains whether an item URL is a document or directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/searchapi/nf-searchapi-iurlaccessor4-shouldindexitemcontent">ShouldIndexItemContent</a>
</td>
<td align="left" width="63%">
Identifies whether the item's content should be indexed. 
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/searchapi/nf-searchapi-iurlaccessor4-shouldindexproperty">ShouldIndexProperty</a>
</td>
<td align="left" width="63%">
Identifies whether a property should be indexed.

</td>
</tr>
</table>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor">IUrlAccessor</a>



<a href="/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor2">IUrlAccessor2</a>



<a href="/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor3">IUrlAccessor3</a>



<b>Reference</b>



<a href="/windows/desktop/search/-search-indexing-process-overview">The Indexing Process</a>