---
UID: NF:searchapi.ISearchCrawlScopeManager.RemoveRoot
title: ISearchCrawlScopeManager::RemoveRoot (searchapi.h)
description: Removes a search root from the search engine.
helpviewer_keywords: ["ISearchCrawlScopeManager interface [search]","RemoveRoot method","ISearchCrawlScopeManager.RemoveRoot","ISearchCrawlScopeManager::RemoveRoot","RemoveRoot","RemoveRoot method [search]","RemoveRoot method [search]","ISearchCrawlScopeManager interface","_search_ISearchCrawlScopeManager_RemoveRoot","search._search_ISearchCrawlScopeManager_RemoveRoot","searchapi/ISearchCrawlScopeManager::RemoveRoot"]
old-location: search\_search_ISearchCrawlScopeManager_RemoveRoot.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchcrawlscopemanager\removeroot.htm
ms.date: 12/05/2018
ms.keywords: ISearchCrawlScopeManager interface [search],RemoveRoot method, ISearchCrawlScopeManager.RemoveRoot, ISearchCrawlScopeManager::RemoveRoot, RemoveRoot, RemoveRoot method [search], RemoveRoot method [search],ISearchCrawlScopeManager interface, _search_ISearchCrawlScopeManager_RemoveRoot, search._search_ISearchCrawlScopeManager_RemoveRoot, searchapi/ISearchCrawlScopeManager::RemoveRoot
f1_keywords:
- searchapi/ISearchCrawlScopeManager.RemoveRoot
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
- ISearchCrawlScopeManager.RemoveRoot
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# ISearchCrawlScopeManager::RemoveRoot


## -description


Removes a search root from the search engine.
        


## -parameters




### -param pszURL [in]

Type: <b>LPCWSTR</b>

The URL of a search root to be removed.
        


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful; S_FALSE if the root is not found.




## -remarks

<b>Windows 7 and later</b>: Check out the <a href="https://docs.microsoft.com/windows/win32/search/-search-sample-crawlscopecommandline">CrawlScopeCommandLine code sample</a> to see how to define command line options for Crawl Scope Manager (CSM) indexing operations.
