---
UID: NN:searchapi.ISearchCrawlScopeManager2
title: ISearchCrawlScopeManager2 (searchapi.h)
description: Extends the functionality of the ISearchCrawlScopeManager interface.
helpviewer_keywords: ["ISearchCrawlScopeManager2","ISearchCrawlScopeManager2 interface [search]","ISearchCrawlScopeManager2 interface [search]","described","_search_ISearchCrawlScopeManager2","search._search_ISearchCrawlScopeManager2","searchapi/ISearchCrawlScopeManager2"]
old-location: search\_search_ISearchCrawlScopeManager2.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\crawlscope\isearchcrawlscopemanager2\isearchcrawlscopemanager2.htm
ms.date: 12/05/2018
ms.keywords: ISearchCrawlScopeManager2, ISearchCrawlScopeManager2 interface [search], ISearchCrawlScopeManager2 interface [search],described, _search_ISearchCrawlScopeManager2, search._search_ISearchCrawlScopeManager2, searchapi/ISearchCrawlScopeManager2
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISearchCrawlScopeManager2
 - searchapi/ISearchCrawlScopeManager2
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
 - ISearchCrawlScopeManager2
---

# ISearchCrawlScopeManager2 interface


## -description

Extends the functionality of the <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager">ISearchCrawlScopeManager</a> interface. <b>ISearchCrawlScopeManager2</b> provides methods that notify the search engine of containers to crawl and/or watch, and items under those containers to include or exclude when crawling or watching.

## -inheritance

The <b>ISearchCrawlScopeManager2</b> interface inherits from <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager">ISearchCrawlScopeManager</a>. <b>ISearchCrawlScopeManager2</b> also has these types of members:

## -remarks

For a sample that demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations, see the [CrawlScopeCommandLine](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/CrawlScopeCommandLine) sample.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager">ISearchCrawlScopeManager</a>



<b>Reference</b>



<a href="/windows/desktop/search/-search-indexing-process-overview">The Indexing process</a>



<a href="/windows/desktop/search/-search-3x-wds-extidx-csm">Using the Crawl Scope Manager</a>
