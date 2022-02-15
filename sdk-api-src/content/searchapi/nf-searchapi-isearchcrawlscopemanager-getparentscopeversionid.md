---
UID: NF:searchapi.ISearchCrawlScopeManager.GetParentScopeVersionId
title: ISearchCrawlScopeManager::GetParentScopeVersionId (searchapi.h)
description: Gets the version ID of the parent inclusion URL.
helpviewer_keywords: ["GetParentScopeVersionId","GetParentScopeVersionId method [search]","GetParentScopeVersionId method [search]","ISearchCrawlScopeManager interface","ISearchCrawlScopeManager interface [search]","GetParentScopeVersionId method","ISearchCrawlScopeManager.GetParentScopeVersionId","ISearchCrawlScopeManager::GetParentScopeVersionId","_search_ISearchCrawlScopeManager_GetParentScopeVersionId","search._search_ISearchCrawlScopeManager_GetParentScopeVersionId","searchapi/ISearchCrawlScopeManager::GetParentScopeVersionId"]
old-location: search\_search_ISearchCrawlScopeManager_GetParentScopeVersionId.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchcrawlscopemanager\getparentscopeversionid.htm
ms.date: 12/05/2018
ms.keywords: GetParentScopeVersionId, GetParentScopeVersionId method [search], GetParentScopeVersionId method [search],ISearchCrawlScopeManager interface, ISearchCrawlScopeManager interface [search],GetParentScopeVersionId method, ISearchCrawlScopeManager.GetParentScopeVersionId, ISearchCrawlScopeManager::GetParentScopeVersionId, _search_ISearchCrawlScopeManager_GetParentScopeVersionId, search._search_ISearchCrawlScopeManager_GetParentScopeVersionId, searchapi/ISearchCrawlScopeManager::GetParentScopeVersionId
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
 - ISearchCrawlScopeManager::GetParentScopeVersionId
 - searchapi/ISearchCrawlScopeManager::GetParentScopeVersionId
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
 - ISearchCrawlScopeManager.GetParentScopeVersionId
---

# ISearchCrawlScopeManager::GetParentScopeVersionId


## -description

Gets the version ID of the parent inclusion URL.

## -parameters

### -param pszURL [in]

Type: <b>LPCWSTR</b>

A string containing the current URL.

### -param plScopeId [out, retval]

Type: <b>LONG*</b>

On return, contains a pointer to the version ID of the parent inclusion  URL for <b>pszUrl</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Use this method to determine whether the indexer is aware of a change in a data store or scope (for example, a data store is removed and then re-added to the index), potentially requiring a new push of the hierarchical parent of the store's URL.

This ID can change if a scope rule is removed and then added again. This method returns <b>S_FALSE</b> if no parent inclusion URL was found.

<b>Windows 7 and later</b>: Check out the <a href="/windows/win32/search/-search-sample-crawlscopecommandline">CrawlScopeCommandLine code sample</a> to see how to define command line options for Crawl Scope Manager (CSM) indexing operations.