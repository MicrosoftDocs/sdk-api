---
UID: NF:searchapi.ISearchCrawlScopeManager.EnumerateScopeRules
title: ISearchCrawlScopeManager::EnumerateScopeRules (searchapi.h)
description: Returns an enumeration of all the scope rules of which this instance of the ISearchCrawlScopeManager interface is aware.
helpviewer_keywords: ["EnumerateScopeRules","EnumerateScopeRules method [search]","EnumerateScopeRules method [search]","ISearchCrawlScopeManager interface","ISearchCrawlScopeManager interface [search]","EnumerateScopeRules method","ISearchCrawlScopeManager.EnumerateScopeRules","ISearchCrawlScopeManager::EnumerateScopeRules","_search_ISearchCrawlScopeManager_EnumerateScopeRules","search._search_ISearchCrawlScopeManager_EnumerateScopeRules","searchapi/ISearchCrawlScopeManager::EnumerateScopeRules"]
old-location: search\_search_ISearchCrawlScopeManager_EnumerateScopeRules.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchcrawlscopemanager\enumeratescoperules.htm
ms.date: 12/05/2018
ms.keywords: EnumerateScopeRules, EnumerateScopeRules method [search], EnumerateScopeRules method [search],ISearchCrawlScopeManager interface, ISearchCrawlScopeManager interface [search],EnumerateScopeRules method, ISearchCrawlScopeManager.EnumerateScopeRules, ISearchCrawlScopeManager::EnumerateScopeRules, _search_ISearchCrawlScopeManager_EnumerateScopeRules, search._search_ISearchCrawlScopeManager_EnumerateScopeRules, searchapi/ISearchCrawlScopeManager::EnumerateScopeRules
f1_keywords:
- searchapi/ISearchCrawlScopeManager.EnumerateScopeRules
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
- ISearchCrawlScopeManager.EnumerateScopeRules
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# ISearchCrawlScopeManager::EnumerateScopeRules


## -description


Returns an enumeration of all the scope rules of which this instance of the <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager">ISearchCrawlScopeManager</a> interface is aware.
        


## -parameters




### -param ppSearchScopeRules [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-ienumsearchscoperules">IEnumSearchScopeRules</a>**</b>

Returns a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-ienumsearchscoperules">IEnumSearchScopeRules</a> interface.
        


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, S_FALSE if there are no rules to enumerate, or an error value otherwise. 
        




## -remarks

<b>Windows 7 and later</b>: Check out the <a href="https://docs.microsoft.com/windows/win32/search/-search-sample-crawlscopecommandline">CrawlScopeCommandLine code sample</a> to see how to define command line options for Crawl Scope Manager (CSM) indexing operations.
