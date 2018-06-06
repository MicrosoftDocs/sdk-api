---
UID: NF:searchapi.ISearchCrawlScopeManager.RemoveScopeRule
title: ISearchCrawlScopeManager::RemoveScopeRule
author: windows-sdk-content
description: Removes a scope rule from the search engine.
old-location: search\_search_ISearchCrawlScopeManager_RemoveScopeRule.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchcrawlscopemanager\removescoperule.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: ISearchCrawlScopeManager interface [search],RemoveScopeRule method, ISearchCrawlScopeManager.RemoveScopeRule, ISearchCrawlScopeManager::RemoveScopeRule, RemoveScopeRule, RemoveScopeRule method [search], RemoveScopeRule method [search],ISearchCrawlScopeManager interface, _search_ISearchCrawlScopeManager_RemoveScopeRule, search._search_ISearchCrawlScopeManager_RemoveScopeRule, searchapi/ISearchCrawlScopeManager::RemoveScopeRule
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
 - ISearchCrawlScopeManager.RemoveScopeRule
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISearchCrawlScopeManager::RemoveScopeRule


## -description


Removes a scope rule from the search engine.


## -parameters




### -param pszRule [in]

Type: <b>LPCWSTR</b>

The URL or pattern of a scope rule to be removed.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful; returns S_FALSE if the scope rule is not found.




## -remarks



URLs passed in as parameters to <b>ISearchCrawlScopeManager::RemoveScopeRule</b> are expected to be fully URL-decoded and without URL control codes. For example, file:///c:\My Documents is fully URL-decoded, whereas file:///c:\My%20Documents is not.

<b>Windows 7 and later</b>: the CrawlScopeCommandLine code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.



