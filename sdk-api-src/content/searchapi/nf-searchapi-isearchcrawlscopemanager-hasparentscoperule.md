---
UID: NF:searchapi.ISearchCrawlScopeManager.HasParentScopeRule
title: ISearchCrawlScopeManager::HasParentScopeRule
author: windows-sdk-content
description: Identifies whether a given URL has a parent rule in scope.
old-location: search\_search_ISearchCrawlScopeManager_HasParentScopeRule.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchcrawlscopemanager\hasparentscoperule.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: HasParentScopeRule, HasParentScopeRule method [search], HasParentScopeRule method [search],ISearchCrawlScopeManager interface, ISearchCrawlScopeManager interface [search],HasParentScopeRule method, ISearchCrawlScopeManager.HasParentScopeRule, ISearchCrawlScopeManager::HasParentScopeRule, _search_ISearchCrawlScopeManager_HasParentScopeRule, search._search_ISearchCrawlScopeManager_HasParentScopeRule, searchapi/ISearchCrawlScopeManager::HasParentScopeRule
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: ROWSETEVENT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Searchapi.h
api_name:
 - ISearchCrawlScopeManager.HasParentScopeRule
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>Windows 7 and later</b>: the CrawlScopeCommandLine code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.



