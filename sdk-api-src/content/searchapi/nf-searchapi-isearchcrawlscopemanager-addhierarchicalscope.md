---
UID: NF:searchapi.ISearchCrawlScopeManager.AddHierarchicalScope
title: ISearchCrawlScopeManager::AddHierarchicalScope (searchapi.h)
description: Adds a hierarchical scope to the search engine.
helpviewer_keywords: ["AddHierarchicalScope","AddHierarchicalScope method [search]","AddHierarchicalScope method [search]","ISearchCrawlScopeManager interface","ISearchCrawlScopeManager interface [search]","AddHierarchicalScope method","ISearchCrawlScopeManager.AddHierarchicalScope","ISearchCrawlScopeManager::AddHierarchicalScope","_search_ISearchCrawlScopeManager_AddHierachicalScope","search._search_ISearchCrawlScopeManager_AddHierachicalScope","searchapi/ISearchCrawlScopeManager::AddHierarchicalScope"]
old-location: search\_search_ISearchCrawlScopeManager_AddHierachicalScope.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchcrawlscopemanager\addhierarchicalscope.htm
ms.date: 12/05/2018
ms.keywords: AddHierarchicalScope, AddHierarchicalScope method [search], AddHierarchicalScope method [search],ISearchCrawlScopeManager interface, ISearchCrawlScopeManager interface [search],AddHierarchicalScope method, ISearchCrawlScopeManager.AddHierarchicalScope, ISearchCrawlScopeManager::AddHierarchicalScope, _search_ISearchCrawlScopeManager_AddHierachicalScope, search._search_ISearchCrawlScopeManager_AddHierachicalScope, searchapi/ISearchCrawlScopeManager::AddHierarchicalScope
f1_keywords:
- searchapi/ISearchCrawlScopeManager.AddHierarchicalScope
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
- ISearchCrawlScopeManager.AddHierarchicalScope
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# ISearchCrawlScopeManager::AddHierarchicalScope


## -description


Adds a hierarchical scope to the search engine.
        


## -parameters




### -param pszURL [in]

Type: <b>LPCWSTR</b>

The URL of the scope to be added.
                


### -param fInclude [in]

Type: <b>BOOL</b>

<b>TRUE</b> if this is an inclusion scope, <b>FALSE</b> if this is an exclusion scope.
                


### -param fDefault [in]

Type: <b>BOOL</b>

<b>TRUE</b> if this is to be the default scope, <b>FALSE</b> if this is not a default scope.
                


### -param fOverrideChildren [in]

Type: <b>BOOL</b>

<b>TRUE</b> if this scope overrides all of the child URL rules, <b>FALSE</b> otherwise.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method overrides existing scope rules for the URL.The preferred methods for such functionality are <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchcrawlscopemanager-adddefaultscoperule">ISearchCrawlScopeManager::AddDefaultScopeRule</a> and <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchcrawlscopemanager-adduserscoperule">ISearchCrawlScopeManager::AddUserScopeRule</a>.

URLs passed in as parameters to <b>ISearchCrawlScopeManager::AddHierarchicalScope</b> are expected to be fully URL-decoded and without URL control codes. For example, file:///c:\My Documents is fully URL-decoded, whereas file:///c:\My%20Documents is not.

<b>Windows 7 and later</b>: the CrawlScopeCommandLine code sample, available on <a href="https://code.msdn.microsoft.com/windowssearch">Code Gallery</a> and the <a href="https://msdn.microsoft.com/windowsvista/bb980924.aspx">Windows 7 SDK</a>, demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.



