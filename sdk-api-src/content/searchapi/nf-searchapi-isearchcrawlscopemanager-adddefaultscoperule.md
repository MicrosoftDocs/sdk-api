---
UID: NF:searchapi.ISearchCrawlScopeManager.AddDefaultScopeRule
title: ISearchCrawlScopeManager::AddDefaultScopeRule (searchapi.h)
author: windows-sdk-content
description: Adds a URL as the default scope for this rule.
old-location: search\_search_ISearchCrawlScopeManager_AddDefaultScopeRule.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchcrawlscopemanager\adddefaultscoperule.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AddDefaultScopeRule, AddDefaultScopeRule method [search], AddDefaultScopeRule method [search],ISearchCrawlScopeManager interface, ISearchCrawlScopeManager interface [search],AddDefaultScopeRule method, ISearchCrawlScopeManager.AddDefaultScopeRule, ISearchCrawlScopeManager::AddDefaultScopeRule, _search_ISearchCrawlScopeManager_AddDefaultScopeRule, search._search_ISearchCrawlScopeManager_AddDefaultScopeRule, searchapi/ISearchCrawlScopeManager::AddDefaultScopeRule
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
 - ISearchCrawlScopeManager.AddDefaultScopeRule
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# ISearchCrawlScopeManager::AddDefaultScopeRule


## -description


Adds a URL as the default scope for this rule.
        


## -parameters




### -param pszURL [in]

Type: <b>LPCWSTR</b>

Pointer to a null-terminated, Unicode buffer that contains the URL to use as a default scope.


### -param fInclude [in]

Type: <b>BOOL</b>

<b>TRUE</b> if <i>pszUrl</i> should be included in indexing; <b>FALSE</b> if it should be excluded.


### -param fFollowFlags [in]

Type: <b>DWORD</b>

Sets the <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/ne-searchapi-_follow_flags">FOLLOW_FLAGS</a> to specify whether to follow complex URLs and whether a URL is to be indexed or just followed.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Default scope rules provide an initial set of scope rules. User scope rules always take precedence over default scope rules, unless user-defined rules are reverted in which case the default scope rules are reinstated.

URLs passed in as parameters to <b>ISearchCrawlScopeManager::AddDefaultScopeRule</b> are expected to be fully URL-decoded and without URL control codes. For example, file:///c:\My Documents is fully URL-decoded, whereas file:///c:\My%20Documents is not.

<b>Windows 7 and later</b>: the CrawlScopeCommandLine code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.



