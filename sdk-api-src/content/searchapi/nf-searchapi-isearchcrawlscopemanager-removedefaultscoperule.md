---
UID: NF:searchapi.ISearchCrawlScopeManager.RemoveDefaultScopeRule
title: ISearchCrawlScopeManager::RemoveDefaultScopeRule (searchapi.h)
description: Removes a default scope rule from the search engine.
helpviewer_keywords: ["ISearchCrawlScopeManager interface [search]","RemoveDefaultScopeRule method","ISearchCrawlScopeManager.RemoveDefaultScopeRule","ISearchCrawlScopeManager::RemoveDefaultScopeRule","RemoveDefaultScopeRule","RemoveDefaultScopeRule method [search]","RemoveDefaultScopeRule method [search]","ISearchCrawlScopeManager interface","_search_ISearchCrawlScopeManager_RemoveDefaultScopeRule","search._search_ISearchCrawlScopeManager_RemoveDefaultScopeRule","searchapi/ISearchCrawlScopeManager::RemoveDefaultScopeRule"]
old-location: search\_search_ISearchCrawlScopeManager_RemoveDefaultScopeRule.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchcrawlscopemanager\removedefaultscoperule.htm
ms.date: 12/05/2018
ms.keywords: ISearchCrawlScopeManager interface [search],RemoveDefaultScopeRule method, ISearchCrawlScopeManager.RemoveDefaultScopeRule, ISearchCrawlScopeManager::RemoveDefaultScopeRule, RemoveDefaultScopeRule, RemoveDefaultScopeRule method [search], RemoveDefaultScopeRule method [search],ISearchCrawlScopeManager interface, _search_ISearchCrawlScopeManager_RemoveDefaultScopeRule, search._search_ISearchCrawlScopeManager_RemoveDefaultScopeRule, searchapi/ISearchCrawlScopeManager::RemoveDefaultScopeRule
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
 - ISearchCrawlScopeManager::RemoveDefaultScopeRule
 - searchapi/ISearchCrawlScopeManager::RemoveDefaultScopeRule
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
 - ISearchCrawlScopeManager.RemoveDefaultScopeRule
---

# ISearchCrawlScopeManager::RemoveDefaultScopeRule


## -description

Removes a default scope rule from the search engine.

## -parameters

### -param pszURL [in]

Type: <b>LPCWSTR</b>

A string identifying the URL or pattern of the default rule to be removed.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error otherwise.

## -remarks

URLs passed in as parameters to <b>ISearchCrawlScopeManager::RemoveDefaultScopeRule</b> are expected to be fully URL-decoded and without URL control codes. For example, file:///c:\My Documents is fully URL-decoded, whereas file:///c:\My%20Documents is not.

<b>Windows 7 and later</b>: Check out the <a href="/windows/win32/search/-search-sample-crawlscopecommandline">CrawlScopeCommandLine code sample</a> to see how to define command line options for Crawl Scope Manager (CSM) indexing operations.