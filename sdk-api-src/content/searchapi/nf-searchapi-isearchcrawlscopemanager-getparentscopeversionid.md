---
UID: NF:searchapi.ISearchCrawlScopeManager.GetParentScopeVersionId
title: ISearchCrawlScopeManager::GetParentScopeVersionId
author: windows-driver-content
description: Gets the version ID of the parent inclusion URL.
old-location: search\_search_ISearchCrawlScopeManager_GetParentScopeVersionId.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchcrawlscopemanager\getparentscopeversionid.htm
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: GetParentScopeVersionId, GetParentScopeVersionId method [search], GetParentScopeVersionId method [search],ISearchCrawlScopeManager interface, ISearchCrawlScopeManager interface [search],GetParentScopeVersionId method, ISearchCrawlScopeManager.GetParentScopeVersionId, ISearchCrawlScopeManager::GetParentScopeVersionId, _search_ISearchCrawlScopeManager_GetParentScopeVersionId, search._search_ISearchCrawlScopeManager_GetParentScopeVersionId, searchapi/ISearchCrawlScopeManager::GetParentScopeVersionId
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
-	ISearchCrawlScopeManager.GetParentScopeVersionId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ISearchCrawlScopeManager::GetParentScopeVersionId


## -description


Gets the version ID of the parent inclusion URL.


## -parameters




### -param pszURL




### -param plScopeId [out, retval]

Type: <b>LONG*</b>

On return, contains a pointer to the version ID of the parent inclusion  URL for <b>pszUrl</b>.


#### - pszUrl [in]

Type: <b>LPCWSTR</b>

A string containing the current URL.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Use this method to determine whether the indexer is aware of a change in a data store or scope (for example, a data store is removed and then re-added to the index), potentially requiring a new push of the hierarchical parent of the store's URL.

This ID can change if a scope rule is removed and then added again. This method returns <b>S_FALSE</b> if no parent inclusion URL was found.

<b>Windows 7 and later</b>: the CrawlScopeCommandLine code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.



