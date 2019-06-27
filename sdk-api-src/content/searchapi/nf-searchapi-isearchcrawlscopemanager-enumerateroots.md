---
UID: NF:searchapi.ISearchCrawlScopeManager.EnumerateRoots
title: ISearchCrawlScopeManager::EnumerateRoots (searchapi.h)
author: windows-sdk-content
description: Returns an enumeration of all the roots of which this instance of the ISearchCrawlScopeManager is aware.
old-location: search\_search_ISearchCrawlScopeManager_EnumerateRoots.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchcrawlscopemanager\enumerateroots.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EnumerateRoots, EnumerateRoots method [search], EnumerateRoots method [search],ISearchCrawlScopeManager interface, ISearchCrawlScopeManager interface [search],EnumerateRoots method, ISearchCrawlScopeManager.EnumerateRoots, ISearchCrawlScopeManager::EnumerateRoots, _search_ISearchCrawlScopeManager_EnumerateRoots, search._search_ISearchCrawlScopeManager_EnumerateRoots, searchapi/ISearchCrawlScopeManager::EnumerateRoots
ms.topic: method
f1_keywords: 
 - "searchapi/ISearchCrawlScopeManager.EnumerateRoots"
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
 - ISearchCrawlScopeManager.EnumerateRoots
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# ISearchCrawlScopeManager::EnumerateRoots


## -description


Returns an enumeration of all the roots of which this instance of the <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager">ISearchCrawlScopeManager</a> is aware.
        


## -parameters




### -param ppSearchRoots [out, retval]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-ienumsearchroots">IEnumSearchRoots</a>**</b>

Returns a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-ienumsearchroots">IEnumSearchRoots</a> interface.
                


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, S_FALSE if there are no roots to enumerate, or an error value otherwise.
                




## -remarks



<i>ppSearchRoots</i> is set to <b>NULL</b> if there are no roots to enumerate.

<b>Windows 7 and later</b>: the CrawlScopeCommandLine code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.



