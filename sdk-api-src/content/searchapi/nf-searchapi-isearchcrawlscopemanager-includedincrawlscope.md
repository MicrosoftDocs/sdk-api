---
UID: NF:searchapi.ISearchCrawlScopeManager.IncludedInCrawlScope
title: ISearchCrawlScopeManager::IncludedInCrawlScope (searchapi.h)
description: Retrieves an indicator of whether the specified URL is included in the crawl scope.
old-location: search\_search_ISearchCrawlScopeManager_IncludedInCrawlScope.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchcrawlscopemanager\includedincrawlscope.htm
ms.date: 12/05/2018
ms.keywords: ISearchCrawlScopeManager interface [search],IncludedInCrawlScope method, ISearchCrawlScopeManager.IncludedInCrawlScope, ISearchCrawlScopeManager::IncludedInCrawlScope, IncludedInCrawlScope, IncludedInCrawlScope method [search], IncludedInCrawlScope method [search],ISearchCrawlScopeManager interface, _search_ISearchCrawlScopeManager_IncludedInCrawlScope, search._search_ISearchCrawlScopeManager_IncludedInCrawlScope, searchapi/ISearchCrawlScopeManager::IncludedInCrawlScope
f1_keywords:
- searchapi/ISearchCrawlScopeManager.IncludedInCrawlScope
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Searchapi.h
api_name:
- ISearchCrawlScopeManager.IncludedInCrawlScope
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# ISearchCrawlScopeManager::IncludedInCrawlScope


## -description


Retrieves an indicator of whether the specified URL is included in the crawl scope.
        


## -parameters




### -param pszURL [in]

Type: <b>LPCWSTR</b>

A string containing the URL to check for inclusion in the crawl scope.
                


### -param pfIsIncluded [out, retval]

Type: <b>BOOL*</b>

A pointer to a <b>BOOL</b> value: <b>TRUE</b> if <i>pszURL</i> is included in the crawl scope; otherwise, <b>FALSE</b>.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For hierarchical sources, the most immediate parent is included. For non-hierarchical sources like URLs, this will be only the URL rule itself. Other URLs that might be indexed will cause this method to retrieve <b>FALSE</b> because there is no way to tell whether they are in the scope.

<b>Windows 7 and later</b>: the CrawlScopeCommandLine code sample, available on <a href="https://code.msdn.microsoft.com/windowssearch">Code Gallery</a> and the <a href="https://msdn.microsoft.com/windowsvista/bb980924.aspx">Windows 7 SDK</a>, demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.



