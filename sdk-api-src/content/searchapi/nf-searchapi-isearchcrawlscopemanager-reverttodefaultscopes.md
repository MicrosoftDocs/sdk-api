---
UID: NF:searchapi.ISearchCrawlScopeManager.RevertToDefaultScopes
title: ISearchCrawlScopeManager::RevertToDefaultScopes (searchapi.h)
description: Reverts to the default scopes.
helpviewer_keywords: ["ISearchCrawlScopeManager interface [search]","RevertToDefaultScopes method","ISearchCrawlScopeManager.RevertToDefaultScopes","ISearchCrawlScopeManager::RevertToDefaultScopes","RevertToDefaultScopes","RevertToDefaultScopes method [search]","RevertToDefaultScopes method [search]","ISearchCrawlScopeManager interface","_search_ISearchCrawlScopeManager_RevertToDefaultScopes","search._search_ISearchCrawlScopeManager_RevertToDefaultScopes","searchapi/ISearchCrawlScopeManager::RevertToDefaultScopes"]
old-location: search\_search_ISearchCrawlScopeManager_RevertToDefaultScopes.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchcrawlscopemanager\reverttodefaultscopes.htm
ms.date: 12/05/2018
ms.keywords: ISearchCrawlScopeManager interface [search],RevertToDefaultScopes method, ISearchCrawlScopeManager.RevertToDefaultScopes, ISearchCrawlScopeManager::RevertToDefaultScopes, RevertToDefaultScopes, RevertToDefaultScopes method [search], RevertToDefaultScopes method [search],ISearchCrawlScopeManager interface, _search_ISearchCrawlScopeManager_RevertToDefaultScopes, search._search_ISearchCrawlScopeManager_RevertToDefaultScopes, searchapi/ISearchCrawlScopeManager::RevertToDefaultScopes
f1_keywords:
- searchapi/ISearchCrawlScopeManager.RevertToDefaultScopes
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
- ISearchCrawlScopeManager.RevertToDefaultScopes
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# ISearchCrawlScopeManager::RevertToDefaultScopes


## -description


Reverts to the default scopes.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks

This method removes all user-defined rules and reverts the working set of crawls scope rules to the default rules.

<b>Windows 7 and later</b>: Check out the <a href="https://docs.microsoft.com/windows/win32/search/-search-sample-crawlscopecommandline">CrawlScopeCommandLine code sample</a> to see how to define command line options for Crawl Scope Manager (CSM) indexing operations.
