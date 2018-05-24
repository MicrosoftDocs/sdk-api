---
UID: NF:searchapi.ISearchCrawlScopeManager.AddRoot
title: ISearchCrawlScopeManager::AddRoot
author: windows-driver-content
description: Adds a new search root to the search engine.
old-location: search\_search_ISearchCrawlScopeManager_AddRoot.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchcrawlscopemanager\addroot.htm
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: AddRoot, AddRoot method [search], AddRoot method [search],ISearchCrawlScopeManager interface, ISearchCrawlScopeManager interface [search],AddRoot method, ISearchCrawlScopeManager.AddRoot, ISearchCrawlScopeManager::AddRoot, _search_ISearchCrawlScopeManager_AddRoot, search._search_ISearchCrawlScopeManager_AddRoot, searchapi/ISearchCrawlScopeManager::AddRoot
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
-	ISearchCrawlScopeManager.AddRoot
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISearchCrawlScopeManager::AddRoot


## -description



            Adds a new search root to the search engine.
        


## -parameters




### -param pSearchRoot [in]

Type: <b><a href="https://msdn.microsoft.com/1df814f4-2403-4a78-bb7d-0e1d98da7265">ISearchRoot</a>*</b>


                    An <a href="https://msdn.microsoft.com/1df814f4-2403-4a78-bb7d-0e1d98da7265">ISearchRoot</a> describing the new search root to add.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Overrides any existing root definition for the URL.

<b>Windows 7 and later</b>: the CrawlScopeCommandLine code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.



