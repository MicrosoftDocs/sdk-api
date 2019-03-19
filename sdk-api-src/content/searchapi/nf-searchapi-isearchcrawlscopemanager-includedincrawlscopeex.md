---
UID: NF:searchapi.ISearchCrawlScopeManager.IncludedInCrawlScopeEx
title: ISearchCrawlScopeManager::IncludedInCrawlScopeEx (searchapi.h)
author: windows-sdk-content
description: Retrieves an indicator of whether and why the specified URL is included in the crawl scope.
old-location: search\_search_ISearchCrawlScopeManager_IncludedInCrawlScopeEx.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchcrawlscopemanager\includedincrawlscopeex.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISearchCrawlScopeManager interface [search],IncludedInCrawlScopeEx method, ISearchCrawlScopeManager.IncludedInCrawlScopeEx, ISearchCrawlScopeManager::IncludedInCrawlScopeEx, IncludedInCrawlScopeEx, IncludedInCrawlScopeEx method [search], IncludedInCrawlScopeEx method [search],ISearchCrawlScopeManager interface, _search_ISearchCrawlScopeManager_IncludedInCrawlScopeEx, search._search_ISearchCrawlScopeManager_IncludedInCrawlScopeEx, searchapi/ISearchCrawlScopeManager::IncludedInCrawlScopeEx
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
 - ISearchCrawlScopeManager.IncludedInCrawlScopeEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# ISearchCrawlScopeManager::IncludedInCrawlScopeEx


## -description


Retrieves an indicator of whether and why the specified URL is included in the crawl scope.


## -parameters




### -param pszURL [in]

Type: <b>LPCWSTR</b>

A string value indicating the URL to check for inclusion in the crawl scope.


### -param pfIsIncluded [out]

Type: <b>BOOL*</b>

A pointer to a <b>BOOL</b> value: <b>TRUE</b> if <i>pszURL</i> is included in the crawl scope; otherwise, <b>FALSE</b>.


### -param pReason [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa965690(v=VS.85).aspx">CLUSION_REASON</a>*</b>

Retrieves a pointer to a value from the <a href="https://msdn.microsoft.com/en-us/library/Aa965690(v=VS.85).aspx">CLUSION_REASON</a> enumeration that indicates the reason that the specified URL was included in or excluded from the crawl scope.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For hierarchical sources, the most immediate parent is included. For non-hierarchical sources like URLs, this will be only the URL rule itself. Other URLs that might be indexed will cause this method to retrieve <b>FALSE</b> because there is no way to tell whether they are in the scope.

<b>Windows 7 and later</b>: the CrawlScopeCommandLine code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.



