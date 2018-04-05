---
UID: NF:searchapi.ISearchCatalogManager.ReindexSearchRoot
title: ISearchCatalogManager::ReindexSearchRoot method
author: windows-driver-content
description: Re-indexes all URLs from a specified root.
old-location: search\_search_ISearchCatalogManager_ReindexSearchRoot.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager\reindexsearchroot.htm
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: ISearchCatalogManager, ISearchCatalogManager interface [search], ReindexSearchRoot method, ISearchCatalogManager::ReindexSearchRoot, ReindexSearchRoot method [search], ReindexSearchRoot method [search], ISearchCatalogManager interface, ReindexSearchRoot,ISearchCatalogManager.ReindexSearchRoot, _search_ISearchCatalogManager_ReindexSearchRoot, search._search_ISearchCatalogManager_ReindexSearchRoot, searchapi/ISearchCatalogManager::ReindexSearchRoot
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
req.idl: Searchcatalog.idl
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
-	ISearchCatalogManager.ReindexSearchRoot
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# ISearchCatalogManager::ReindexSearchRoot method


## -description


Re-indexes all URLs from a specified root.


## -parameters




### -param pszRootURL [in]

Type: <b>LPCWSTR</b>


                    Pointer to a null-terminated, Unicode buffer that contains the URL on which the search is rooted. This URL must be a search root previously registered with <a href="https://msdn.microsoft.com/6ce5e2c5-0c33-42a0-8807-eb64881b03af">ISearchCrawlScopeManager::AddRoot</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The indexer begins an incremental crawl of all start pages under <i>pszRootURL</i> upon successful return of method.

Old information remains in the catalog until replaced by new information during the re-indexing.



