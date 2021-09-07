---
UID: NF:searchapi.ISearchCatalogManager.Reset
title: ISearchCatalogManager::Reset (searchapi.h)
description: Resets the underlying catalog by rebuilding the databases and performing a full indexing.
helpviewer_keywords: ["ISearchCatalogManager interface [search]","Reset method","ISearchCatalogManager.Reset","ISearchCatalogManager::Reset","Reset","Reset method [search]","Reset method [search]","ISearchCatalogManager interface","_search_ISearchCatalogManager_Reset","search._search_ISearchCatalogManager_Reset","searchapi/ISearchCatalogManager::Reset"]
old-location: search\_search_ISearchCatalogManager_Reset.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager\reset.htm
ms.date: 12/05/2018
ms.keywords: ISearchCatalogManager interface [search],Reset method, ISearchCatalogManager.Reset, ISearchCatalogManager::Reset, Reset, Reset method [search], Reset method [search],ISearchCatalogManager interface, _search_ISearchCatalogManager_Reset, search._search_ISearchCatalogManager_Reset, searchapi/ISearchCatalogManager::Reset
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
 - ISearchCatalogManager::Reset
 - searchapi/ISearchCatalogManager::Reset
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
 - ISearchCatalogManager.Reset
---

# ISearchCatalogManager::Reset


## -description

Resets the underlying catalog by rebuilding the databases and performing a full indexing.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Resetting can take a very long time, during which little or no information is available to be searched.

