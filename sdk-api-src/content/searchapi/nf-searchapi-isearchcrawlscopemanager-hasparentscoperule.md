---
UID: NF:searchapi.ISearchCrawlScopeManager.HasParentScopeRule
title: ISearchCrawlScopeManager::HasParentScopeRule (searchapi.h)
description: Identifies whether a given URL has a parent rule in scope.
helpviewer_keywords: ["HasParentScopeRule","HasParentScopeRule method [search]","HasParentScopeRule method [search]","ISearchCrawlScopeManager interface","ISearchCrawlScopeManager interface [search]","HasParentScopeRule method","ISearchCrawlScopeManager.HasParentScopeRule","ISearchCrawlScopeManager::HasParentScopeRule","_search_ISearchCrawlScopeManager_HasParentScopeRule","search._search_ISearchCrawlScopeManager_HasParentScopeRule","searchapi/ISearchCrawlScopeManager::HasParentScopeRule"]
old-location: search\_search_ISearchCrawlScopeManager_HasParentScopeRule.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchcrawlscopemanager\hasparentscoperule.htm
ms.date: 12/05/2018
ms.keywords: HasParentScopeRule, HasParentScopeRule method [search], HasParentScopeRule method [search],ISearchCrawlScopeManager interface, ISearchCrawlScopeManager interface [search],HasParentScopeRule method, ISearchCrawlScopeManager.HasParentScopeRule, ISearchCrawlScopeManager::HasParentScopeRule, _search_ISearchCrawlScopeManager_HasParentScopeRule, search._search_ISearchCrawlScopeManager_HasParentScopeRule, searchapi/ISearchCrawlScopeManager::HasParentScopeRule
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
 - ISearchCrawlScopeManager::HasParentScopeRule
 - searchapi/ISearchCrawlScopeManager::HasParentScopeRule
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
 - ISearchCrawlScopeManager.HasParentScopeRule
---

# ISearchCrawlScopeManager::HasParentScopeRule


## -description

Identifies whether a given URL has a parent rule in scope.

## -parameters

### -param pszURL [in]

Type: <b>LPCWSTR</b>

A string containing the URL to check for a parent rule.  The string can contain wildcard characters, such as asterisks (*).

### -param pfHasParentRule [out, retval]

Type: <b>BOOL*</b>

<b>TRUE</b> if <i>pszURL</i> has a parent rule; otherwise, <b>FALSE</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>Windows 7 and later</b>: Check out the <a href="/windows/win32/search/-search-sample-crawlscopecommandline">CrawlScopeCommandLine code sample</a> to see how to define command line options for Crawl Scope Manager (CSM) indexing operations.