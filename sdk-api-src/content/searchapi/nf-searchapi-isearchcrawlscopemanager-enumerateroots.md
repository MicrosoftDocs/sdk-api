---
UID: NF:searchapi.ISearchCrawlScopeManager.EnumerateRoots
title: ISearchCrawlScopeManager::EnumerateRoots
author: windows-sdk-content
description: Returns an enumeration of all the roots of which this instance of the ISearchCrawlScopeManager is aware.
old-location: search\_search_ISearchCrawlScopeManager_EnumerateRoots.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchcrawlscopemanager\enumerateroots.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: EnumerateRoots, EnumerateRoots method [search], EnumerateRoots method [search],ISearchCrawlScopeManager interface, ISearchCrawlScopeManager interface [search],EnumerateRoots method, ISearchCrawlScopeManager.EnumerateRoots, ISearchCrawlScopeManager::EnumerateRoots, _search_ISearchCrawlScopeManager_EnumerateRoots, search._search_ISearchCrawlScopeManager_EnumerateRoots, searchapi/ISearchCrawlScopeManager::EnumerateRoots
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
 - ISearchCrawlScopeManager.EnumerateRoots
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
- ISearchCrawlScopeManager.EnumerateRoots
: 
---

# ISearchCrawlScopeManager::EnumerateRoots


## -description


Returns an enumeration of all the roots of which this instance of the <a href="https://msdn.microsoft.com/8b731941-f1f6-402e-8cee-3c493e3c369d">ISearchCrawlScopeManager</a> is aware.
        


## -parameters




### -param ppSearchRoots [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4fac0cf0-165d-45f2-8e63-02f0c8eae431">IEnumSearchRoots</a>**</b>

Returns a pointer to an <a href="https://msdn.microsoft.com/4fac0cf0-165d-45f2-8e63-02f0c8eae431">IEnumSearchRoots</a> interface.
                


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, S_FALSE if there are no roots to enumerate, or an error value otherwise.
                




## -remarks



<i>ppSearchRoots</i> is set to <b>NULL</b> if there are no roots to enumerate.

<b>Windows 7 and later</b>: the CrawlScopeCommandLine code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.



