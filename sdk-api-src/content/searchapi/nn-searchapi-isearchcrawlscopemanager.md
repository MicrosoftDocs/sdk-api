---
UID: NN:searchapi.ISearchCrawlScopeManager
title: ISearchCrawlScopeManager (searchapi.h)
description: Provides methods that notify the search engine of containers to crawl and/or watch, and items under those containers to include or exclude when crawling or watching.
helpviewer_keywords: ["ISearchCrawlScopeManager","ISearchCrawlScopeManager interface [search]","ISearchCrawlScopeManager interface [search]","described","_search_ISearchCrawlScopeManager","search._search_ISearchCrawlScopeManager","searchapi/ISearchCrawlScopeManager"]
old-location: search\_search_ISearchCrawlScopeManager.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchcrawlscopemanager\isearchcrawlscopemanager.htm
ms.date: 12/05/2018
ms.keywords: ISearchCrawlScopeManager, ISearchCrawlScopeManager interface [search], ISearchCrawlScopeManager interface [search],described, _search_ISearchCrawlScopeManager, search._search_ISearchCrawlScopeManager, searchapi/ISearchCrawlScopeManager
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Searchcrawlscopemanager.idl
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
 - ISearchCrawlScopeManager
 - searchapi/ISearchCrawlScopeManager
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
 - ISearchCrawlScopeManager
---

# ISearchCrawlScopeManager interface


## -description

Provides methods that notify the search engine of containers to crawl and/or watch, and items under those containers to include or exclude when crawling or watching.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISearchCrawlScopeManager</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISearchCrawlScopeManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -remarks

For a sample that demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations, see the [CrawlScopeCommandLine](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/CrawlScopeCommandLine) sample.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/search/-search-indexing-process-overview">The Indexing Process</a>



<a href="/windows/desktop/search/-search-3x-wds-extidx-csm">Using the Crawl Scope Manager</a>
