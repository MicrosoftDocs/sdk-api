---
UID: NN:searchapi.ISearchCatalogManager2
title: ISearchCatalogManager2 (searchapi.h)
description: Extends the ISearchCatalogManager interface to manage a search catalog, for purposes such as re-indexing or setting timeouts.
helpviewer_keywords: ["ISearchCatalogManager2","ISearchCatalogManager2 interface [search]","ISearchCatalogManager2 interface [search]","described","_search_ISearchCatalogManager2","search._search_ISearchCatalogManager2","searchapi/ISearchCatalogManager2"]
old-location: search\_search_ISearchCatalogManager2.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager2\isearchcatalogmanager2.htm
ms.date: 12/05/2018
ms.keywords: ISearchCatalogManager2, ISearchCatalogManager2 interface [search], ISearchCatalogManager2 interface [search],described, _search_ISearchCatalogManager2, search._search_ISearchCatalogManager2, searchapi/ISearchCatalogManager2
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
targetos: Windows
req.typenames: 
req.redist: Windows Search (WS) 4.0
ms.custom: 19H1
f1_keywords:
 - ISearchCatalogManager2
 - searchapi/ISearchCatalogManager2
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
 - ISearchCatalogManager2
---

# ISearchCatalogManager2 interface


## -description

Extends the <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a> interface to manage a search catalog, for purposes such as re-indexing or setting timeouts. Applications can use this interface to attempt to reindex items that failed to be indexed previously, using the <a href="/windows/desktop/api/searchapi/nf-searchapi-isearchcatalogmanager2-prioritizematchingurls">PrioritizeMatchingURLs</a>.

## -inheritance

The <b>ISearchCatalogManager2</b> interface inherits from <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a>. <b>ISearchCatalogManager2</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a>



<a href="/windows/desktop/search/-search-indexing-process-overview">The Indexing Process</a>
