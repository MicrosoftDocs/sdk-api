---
UID: NF:searchapi.ISearchCatalogManager.GetCrawlScopeManager
title: ISearchCatalogManager::GetCrawlScopeManager (searchapi.h)
description: Gets an ISearchCrawlScopeManager interface for this search catalog.
helpviewer_keywords: ["GetCrawlScopeManager","GetCrawlScopeManager method [search]","GetCrawlScopeManager method [search]","ISearchCatalogManager interface","ISearchCatalogManager interface [search]","GetCrawlScopeManager method","ISearchCatalogManager.GetCrawlScopeManager","ISearchCatalogManager::GetCrawlScopeManager","_search_ISearchCatalogManager_GetCrawlScopeManager","search._search_ISearchCatalogManager_GetCrawlScopeManager","searchapi/ISearchCatalogManager::GetCrawlScopeManager"]
old-location: search\_search_ISearchCatalogManager_GetCrawlScopeManager.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager\getcrawlscopemanager.htm
ms.date: 12/05/2018
ms.keywords: GetCrawlScopeManager, GetCrawlScopeManager method [search], GetCrawlScopeManager method [search],ISearchCatalogManager interface, ISearchCatalogManager interface [search],GetCrawlScopeManager method, ISearchCatalogManager.GetCrawlScopeManager, ISearchCatalogManager::GetCrawlScopeManager, _search_ISearchCatalogManager_GetCrawlScopeManager, search._search_ISearchCatalogManager_GetCrawlScopeManager, searchapi/ISearchCatalogManager::GetCrawlScopeManager
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - ISearchCatalogManager::GetCrawlScopeManager
 - searchapi/ISearchCatalogManager::GetCrawlScopeManager
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Searchapi.h
api_name:
 - ISearchCatalogManager.GetCrawlScopeManager
---

# ISearchCatalogManager::GetCrawlScopeManager


## -description

Gets an <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager">ISearchCrawlScopeManager</a> interface for this search catalog.

## -parameters

### -param ppCrawlScopeManager [out, retval]

Type: <b><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager">ISearchCrawlScopeManager</a>**</b>

Receives a pointer to a new <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager">ISearchCrawlScopeManager</a> interface.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.