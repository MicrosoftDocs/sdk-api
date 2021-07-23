---
UID: NF:searchapi.ISearchCatalogManager.get_Name
title: ISearchCatalogManager::get_Name (searchapi.h)
description: Gets the name of the current catalog.
helpviewer_keywords: ["ISearchCatalogManager interface [search]","get_Name method","ISearchCatalogManager.get_Name","ISearchCatalogManager::get_Name","_search_ISearchCatalogManager_get_Name","get_Name","get_Name method [search]","get_Name method [search]","ISearchCatalogManager interface","search._search_ISearchCatalogManager_get_Name","searchapi/ISearchCatalogManager::get_Name"]
old-location: search\_search_ISearchCatalogManager_get_Name.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager\get_name.htm
ms.date: 12/05/2018
ms.keywords: ISearchCatalogManager interface [search],get_Name method, ISearchCatalogManager.get_Name, ISearchCatalogManager::get_Name, _search_ISearchCatalogManager_get_Name, get_Name, get_Name method [search], get_Name method [search],ISearchCatalogManager interface, search._search_ISearchCatalogManager_get_Name, searchapi/ISearchCatalogManager::get_Name
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
 - ISearchCatalogManager::get_Name
 - searchapi/ISearchCatalogManager::get_Name
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
 - ISearchCatalogManager.get_Name
---

# ISearchCatalogManager::get_Name


## -description

Gets the name of the current catalog.

## -parameters

### -param pszName [out, retval]

Type: <b>LPCWSTR*</b>

Receives a pointer to a null-terminated Unicode buffer that contains the name of the current catalog.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

