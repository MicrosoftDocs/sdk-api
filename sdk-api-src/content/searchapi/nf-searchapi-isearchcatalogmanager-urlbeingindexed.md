---
UID: NF:searchapi.ISearchCatalogManager.URLBeingIndexed
title: ISearchCatalogManager::URLBeingIndexed (searchapi.h)
description: Gets the URL that is currently being indexed. If no indexing is currently in process, pszUrl is set to NULL.helpviewer_keywords: ["ISearchCatalogManager interface [search]","URLBeingIndexed method","ISearchCatalogManager.URLBeingIndexed","ISearchCatalogManager::URLBeingIndexed","URLBeingIndexed","URLBeingIndexed method [search]","URLBeingIndexed method [search]","ISearchCatalogManager interface","_search_ISearchCatalogManager_URLBeingIndexed","search._search_ISearchCatalogManager_URLBeingIndexed","searchapi/ISearchCatalogManager::URLBeingIndexed"]
old-location: search\_search_ISearchCatalogManager_URLBeingIndexed.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager\urlbeingindexed.htm
ms.date: 12/05/2018
ms.keywords: ISearchCatalogManager interface [search],URLBeingIndexed method, ISearchCatalogManager.URLBeingIndexed, ISearchCatalogManager::URLBeingIndexed, URLBeingIndexed, URLBeingIndexed method [search], URLBeingIndexed method [search],ISearchCatalogManager interface, _search_ISearchCatalogManager_URLBeingIndexed, search._search_ISearchCatalogManager_URLBeingIndexed, searchapi/ISearchCatalogManager::URLBeingIndexed
f1_keywords:
- searchapi/ISearchCatalogManager.URLBeingIndexed
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Searchapi.h
api_name:
- ISearchCatalogManager.URLBeingIndexed
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# ISearchCatalogManager::URLBeingIndexed


## -description


Gets the URL that is currently being indexed. If no indexing is currently in process, <i>pszUrl</i> is set to <b>NULL</b>.
        


## -parameters




### -param pszUrl [out, retval]

Type: <b>LPWSTR*</b>

Receives a pointer to the URL that is currently being indexed.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



