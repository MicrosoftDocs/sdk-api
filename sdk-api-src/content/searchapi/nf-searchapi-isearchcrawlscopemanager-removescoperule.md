---
UID: NF:searchapi.ISearchCrawlScopeManager.RemoveScopeRule
title: ISearchCrawlScopeManager::RemoveScopeRule (searchapi.h)
description: Removes a scope rule from the search engine.
helpviewer_keywords: ["ISearchCrawlScopeManager interface [search]","RemoveScopeRule method","ISearchCrawlScopeManager.RemoveScopeRule","ISearchCrawlScopeManager::RemoveScopeRule","RemoveScopeRule","RemoveScopeRule method [search]","RemoveScopeRule method [search]","ISearchCrawlScopeManager interface","_search_ISearchCrawlScopeManager_RemoveScopeRule","search._search_ISearchCrawlScopeManager_RemoveScopeRule","searchapi/ISearchCrawlScopeManager::RemoveScopeRule"]
old-location: search\_search_ISearchCrawlScopeManager_RemoveScopeRule.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchcrawlscopemanager\removescoperule.htm
ms.date: 12/05/2018
ms.keywords: ISearchCrawlScopeManager interface [search],RemoveScopeRule method, ISearchCrawlScopeManager.RemoveScopeRule, ISearchCrawlScopeManager::RemoveScopeRule, RemoveScopeRule, RemoveScopeRule method [search], RemoveScopeRule method [search],ISearchCrawlScopeManager interface, _search_ISearchCrawlScopeManager_RemoveScopeRule, search._search_ISearchCrawlScopeManager_RemoveScopeRule, searchapi/ISearchCrawlScopeManager::RemoveScopeRule
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
 - ISearchCrawlScopeManager::RemoveScopeRule
 - searchapi/ISearchCrawlScopeManager::RemoveScopeRule
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
 - ISearchCrawlScopeManager.RemoveScopeRule
---

# ISearchCrawlScopeManager::RemoveScopeRule


## -description

Removes a scope rule from the search engine.

## -parameters

### -param pszRule [in]

Type: <b>LPCWSTR</b>

The URL or pattern of a scope rule to be removed.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful; returns S_FALSE if the scope rule is not found.

## -remarks

URLs passed in as parameters to <b>ISearchCrawlScopeManager::RemoveScopeRule</b> are expected to be fully URL-decoded and without URL control codes. For example, file:///c:\My Documents is fully URL-decoded, whereas file:///c:\My%20Documents is not.

<b>Windows 7 and later</b>: Check out the <a href="/windows/win32/search/-search-sample-crawlscopecommandline">CrawlScopeCommandLine code sample</a> to see how to define command line options for Crawl Scope Manager (CSM) indexing operations.