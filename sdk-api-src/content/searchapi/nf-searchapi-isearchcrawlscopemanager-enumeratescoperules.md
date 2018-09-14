---
UID: NF:searchapi.ISearchCrawlScopeManager.EnumerateScopeRules
title: ISearchCrawlScopeManager::EnumerateScopeRules
author: windows-sdk-content
description: Returns an enumeration of all the scope rules of which this instance of the ISearchCrawlScopeManager interface is aware.
old-location: search\_search_ISearchCrawlScopeManager_EnumerateScopeRules.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchcrawlscopemanager\enumeratescoperules.htm
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: EnumerateScopeRules, EnumerateScopeRules method [search], EnumerateScopeRules method [search],ISearchCrawlScopeManager interface, ISearchCrawlScopeManager interface [search],EnumerateScopeRules method, ISearchCrawlScopeManager.EnumerateScopeRules, ISearchCrawlScopeManager::EnumerateScopeRules, _search_ISearchCrawlScopeManager_EnumerateScopeRules, search._search_ISearchCrawlScopeManager_EnumerateScopeRules, searchapi/ISearchCrawlScopeManager::EnumerateScopeRules
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
 - ISearchCrawlScopeManager.EnumerateScopeRules
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# ISearchCrawlScopeManager::EnumerateScopeRules


## -description


Returns an enumeration of all the scope rules of which this instance of the <a href="https://msdn.microsoft.com/8b731941-f1f6-402e-8cee-3c493e3c369d">ISearchCrawlScopeManager</a> interface is aware.
        


## -parameters




### -param ppSearchScopeRules [out]

Type: <b><a href="https://msdn.microsoft.com/9e285532-8f03-4572-b908-a67abd842268">IEnumSearchScopeRules</a>**</b>

Returns a pointer to an <a href="https://msdn.microsoft.com/9e285532-8f03-4572-b908-a67abd842268">IEnumSearchScopeRules</a> interface.
        


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, S_FALSE if there are no rules to enumerate, or an error value otherwise. 
        




## -remarks



<b>Windows 7 and later</b>: the CrawlScopeCommandLine code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.



