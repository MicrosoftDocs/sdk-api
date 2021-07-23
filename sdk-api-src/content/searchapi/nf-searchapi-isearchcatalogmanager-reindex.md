---
UID: NF:searchapi.ISearchCatalogManager.Reindex
title: ISearchCatalogManager::Reindex (searchapi.h)
description: Re-indexes all URLs in the catalog.
helpviewer_keywords: ["ISearchCatalogManager interface [search]","Reindex method","ISearchCatalogManager.Reindex","ISearchCatalogManager::Reindex","Reindex","Reindex method [search]","Reindex method [search]","ISearchCatalogManager interface","_search_ISearchCatalogManager_Reindex","search._search_ISearchCatalogManager_Reindex","searchapi/ISearchCatalogManager::Reindex"]
old-location: search\_search_ISearchCatalogManager_Reindex.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager\reindex.htm
ms.date: 12/05/2018
ms.keywords: ISearchCatalogManager interface [search],Reindex method, ISearchCatalogManager.Reindex, ISearchCatalogManager::Reindex, Reindex, Reindex method [search], Reindex method [search],ISearchCatalogManager interface, _search_ISearchCatalogManager_Reindex, search._search_ISearchCatalogManager_Reindex, searchapi/ISearchCatalogManager::Reindex
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
 - ISearchCatalogManager::Reindex
 - searchapi/ISearchCatalogManager::Reindex
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
 - ISearchCatalogManager.Reindex
---

# ISearchCatalogManager::Reindex


## -description

Re-indexes all URLs in the catalog.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Old information remains in the catalog until replaced by new information during re-indexing.

