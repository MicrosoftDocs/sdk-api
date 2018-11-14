---
UID: NF:searchapi.ISearchCrawlScopeManager.HasChildScopeRule
title: ISearchCrawlScopeManager::HasChildScopeRule
author: windows-sdk-content
description: Identifies whether a given URL has a child rule in scope.
old-location: search\_search_ISearchCrawlScopeManager_HasChildScopeRule.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchcrawlscopemanager\haschildscoperule.htm
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: HasChildScopeRule, HasChildScopeRule method [search], HasChildScopeRule method [search],ISearchCrawlScopeManager interface, ISearchCrawlScopeManager interface [search],HasChildScopeRule method, ISearchCrawlScopeManager.HasChildScopeRule, ISearchCrawlScopeManager::HasChildScopeRule, _search_ISearchCrawlScopeManager_HasChildScopeRule, search._search_ISearchCrawlScopeManager_HasChildScopeRule, searchapi/ISearchCrawlScopeManager::HasChildScopeRule
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
 - ISearchCrawlScopeManager.HasChildScopeRule
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
- apiref
: 
- COM
: 
- searchapi.h
: 
- ISearchCrawlScopeManager.HasChildScopeRule
: 
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>Windows 7 and later</b>: the CrawlScopeCommandLine code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.



