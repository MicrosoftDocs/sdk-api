---
UID: NF:searchapi.ISearchCrawlScopeManager.RevertToDefaultScopes
title: ISearchCrawlScopeManager::RevertToDefaultScopes method
author: windows-driver-content
description: Reverts to the default scopes.
old-location: search\_search_ISearchCrawlScopeManager_RevertToDefaultScopes.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchcrawlscopemanager\reverttodefaultscopes.htm
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: ISearchCrawlScopeManager, ISearchCrawlScopeManager interface [search], RevertToDefaultScopes method, ISearchCrawlScopeManager::RevertToDefaultScopes, RevertToDefaultScopes method [search], RevertToDefaultScopes method [search], ISearchCrawlScopeManager interface, RevertToDefaultScopes,ISearchCrawlScopeManager.RevertToDefaultScopes, _search_ISearchCrawlScopeManager_RevertToDefaultScopes, search._search_ISearchCrawlScopeManager_RevertToDefaultScopes, searchapi/ISearchCrawlScopeManager::RevertToDefaultScopes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: ROWSETEVENT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Searchapi.h
api_name:
-	ISearchCrawlScopeManager.RevertToDefaultScopes
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ISearchCrawlScopeManager::RevertToDefaultScopes method


## -description


Reverts to the default scopes.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method removes all user-defined rules and reverts the working set of crawls scope rules to the default rules.

<b>Windows 7 and later</b>: the CrawlScopeCommandLine code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.



