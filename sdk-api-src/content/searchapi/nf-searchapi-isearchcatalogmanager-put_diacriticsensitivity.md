---
UID: NF:searchapi.ISearchCatalogManager.put_DiacriticSensitivity
title: ISearchCatalogManager::put_DiacriticSensitivity (searchapi.h)
description: Sets a value that determines whether the catalog is sensitive to diacritics. A diacritic is a mark added to a letter to indicate a special phonetic value or pronunciation.
helpviewer_keywords: ["ISearchCatalogManager interface [search]","put_DiacriticSensitivity method","ISearchCatalogManager.put_DiacriticSensitivity","ISearchCatalogManager::put_DiacriticSensitivity","_search_ISearchCatalogManager_put_DiacriticSensitivity","put_DiacriticSensitivity","put_DiacriticSensitivity method [search]","put_DiacriticSensitivity method [search]","ISearchCatalogManager interface","search._search_ISearchCatalogManager_put_DiacriticSensitivity","searchapi/ISearchCatalogManager::put_DiacriticSensitivity"]
old-location: search\_search_ISearchCatalogManager_put_DiacriticSensitivity.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager\put_diacriticsensitivity.htm
ms.date: 12/05/2018
ms.keywords: ISearchCatalogManager interface [search],put_DiacriticSensitivity method, ISearchCatalogManager.put_DiacriticSensitivity, ISearchCatalogManager::put_DiacriticSensitivity, _search_ISearchCatalogManager_put_DiacriticSensitivity, put_DiacriticSensitivity, put_DiacriticSensitivity method [search], put_DiacriticSensitivity method [search],ISearchCatalogManager interface, search._search_ISearchCatalogManager_put_DiacriticSensitivity, searchapi/ISearchCatalogManager::put_DiacriticSensitivity
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
 - ISearchCatalogManager::put_DiacriticSensitivity
 - searchapi/ISearchCatalogManager::put_DiacriticSensitivity
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
 - ISearchCatalogManager.put_DiacriticSensitivity
---

# ISearchCatalogManager::put_DiacriticSensitivity


## -description

Sets a value that determines whether the catalog is sensitive to diacritics. A diacritic is a mark added to a letter to indicate a special phonetic value or pronunciation.

## -parameters

### -param fDiacriticSensitive [in]

Type: <b>BOOL</b>

A Boolean value that determines whether the catalog is sensitive to diacritics. <b>TRUE</b> if the catalog is sensitive to and recognizes diacritics; otherwise, <b>FALSE</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

