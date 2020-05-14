---
UID: NN:searchapi.IUrlAccessor3
title: IUrlAccessor3 (searchapi.h)
description: Extends the functionality of the IUrlAccessor2 interface with the IUrlAccessor3::GetImpersonationSidBlobs method to identify user security identifiers (SIDs) for a specified URL.helpviewer_keywords: ["IUrlAccessor3","IUrlAccessor3 interface [search]","IUrlAccessor3 interface [search]","described","_search_IUrlAccessor3","search._search_IUrlAccessor3","searchapi/IUrlAccessor3"]
old-location: search\_search_IUrlAccessor3.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\protocolhandlers\iurlaccessor3\iurlaccessor3.htm
ms.date: 12/05/2018
ms.keywords: IUrlAccessor3, IUrlAccessor3 interface [search], IUrlAccessor3 interface [search],described, _search_IUrlAccessor3, search._search_IUrlAccessor3, searchapi/IUrlAccessor3
f1_keywords:
- searchapi/IUrlAccessor3
dev_langs:
- c++
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Searchapi.h
api_name:
- IUrlAccessor3
targetos: Windows
req.typenames: 
req.redist: Windows Search (WS) 4.0
ms.custom: 19H1
---

# IUrlAccessor3 interface


## -description


Extends the functionality of the <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor2">IUrlAccessor2</a> interface with the <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-iurlaccessor3-getimpersonationsidblobs">IUrlAccessor3::GetImpersonationSidBlobs</a> method to identify user security identifiers (SIDs) for a specified URL.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUrlAccessor3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor2">IUrlAccessor2</a>. <b>IUrlAccessor3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUrlAccessor3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-iurlaccessor3-getimpersonationsidblobs">GetImpersonationSidBlobs</a>
</td>
<td align="left" width="63%">
Retrieves an array of user SIDs for a specified URL. This method enables protocol handlers to specify which users can access the file and the search protocol host to impersonate a user in order to index the file.
        

</td>
</tr>
</table> 


## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor">IUrlAccessor</a>



<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor2">IUrlAccessor2</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/search/-search-prth-error-constants">Search Protocol Handler Error Messages</a>



<a href="https://docs.microsoft.com/windows/desktop/search/-search-indexing-process-overview">The Indexing Process</a>
 

 

