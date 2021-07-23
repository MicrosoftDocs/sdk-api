---
UID: NF:searchapi.ISearchCrawlScopeManager.HasChildScopeRule
title: ISearchCrawlScopeManager::HasChildScopeRule (searchapi.h)
description: Identifies whether a given URL has a child rule in scope.
helpviewer_keywords: ["HasChildScopeRule","HasChildScopeRule method [search]","HasChildScopeRule method [search]","ISearchCrawlScopeManager interface","ISearchCrawlScopeManager interface [search]","HasChildScopeRule method","ISearchCrawlScopeManager.HasChildScopeRule","ISearchCrawlScopeManager::HasChildScopeRule","_search_ISearchCrawlScopeManager_HasChildScopeRule","search._search_ISearchCrawlScopeManager_HasChildScopeRule","searchapi/ISearchCrawlScopeManager::HasChildScopeRule"]
old-location: search\_search_ISearchCrawlScopeManager_HasChildScopeRule.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchcrawlscopemanager\haschildscoperule.htm
ms.date: 12/05/2018
ms.keywords: HasChildScopeRule, HasChildScopeRule method [search], HasChildScopeRule method [search],ISearchCrawlScopeManager interface, ISearchCrawlScopeManager interface [search],HasChildScopeRule method, ISearchCrawlScopeManager.HasChildScopeRule, ISearchCrawlScopeManager::HasChildScopeRule, _search_ISearchCrawlScopeManager_HasChildScopeRule, search._search_ISearchCrawlScopeManager_HasChildScopeRule, searchapi/ISearchCrawlScopeManager::HasChildScopeRule
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
 - ISearchCrawlScopeManager::HasChildScopeRule
 - searchapi/ISearchCrawlScopeManager::HasChildScopeRule
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
 - ISearchCrawlScopeManager.HasChildScopeRule
---

# ISearchCrawlScopeManager::HasChildScopeRule


## -description

Identifies whether a given URL has a child rule in scope.

## -parameters

### -param pszURL [in]

Type: <b>LPCWSTR</b>

A string containing the URL to check for a child rule. The string can contain wildcard characters, such as asterisks (*).

### -param pfHasChildRule [out, retval]

Type: <b>BOOL*</b>

<b>TRUE</b> if <i>pszURL</i> has a child rule; otherwise, <b>FALSE</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>Windows 7 and later</b>: Check out the <a href="/windows/win32/search/-search-sample-crawlscopecommandline">CrawlScopeCommandLine code sample</a> to see how to define command line options for Crawl Scope Manager (CSM) indexing operations.