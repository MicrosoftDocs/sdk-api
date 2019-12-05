---
UID: NN:searchapi.ISearchCatalogManager2
title: ISearchCatalogManager2 (searchapi.h)
description: Extends the ISearchCatalogManager interface to manage a search catalog, for purposes such as re-indexing or setting timeouts.
old-location: search\_search_ISearchCatalogManager2.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager2\isearchcatalogmanager2.htm
ms.date: 12/05/2018
ms.keywords: ISearchCatalogManager2, ISearchCatalogManager2 interface [search], ISearchCatalogManager2 interface [search],described, _search_ISearchCatalogManager2, search._search_ISearchCatalogManager2, searchapi/ISearchCatalogManager2
ms.topic: interface
f1_keywords:
- searchapi/ISearchCatalogManager2
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
req.idl: Searchcatalog.idl
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
- ISearchCatalogManager2
targetos: Windows
req.typenames: 
req.redist: Windows Search (WS) 4.0
ms.custom: 19H1
---

# ISearchCatalogManager2 interface


## -description


Extends the <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a> interface to manage a search catalog, for purposes such as re-indexing or setting timeouts. Applications can use this interface to attempt to reindex items that failed to be indexed previously, using the <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchcatalogmanager2-prioritizematchingurls">PrioritizeMatchingURLs</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISearchCatalogManager2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a>. <b>ISearchCatalogManager2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISearchCatalogManager2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchcatalogmanager2-prioritizematchingurls">PrioritizeMatchingURLs</a>
</td>
<td align="left" width="63%">
Instructs the indexer to give a higher priority to indexing items that have URLs that match a specified pattern. These items will then have a higher priority than other indexing tasks.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a>



<a href="https://docs.microsoft.com/windows/desktop/search/-search-indexing-process-overview">The Indexing Process</a>
 

 

