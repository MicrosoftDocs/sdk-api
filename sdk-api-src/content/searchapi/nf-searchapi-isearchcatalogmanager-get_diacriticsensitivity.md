---
UID: NF:searchapi.ISearchCatalogManager.get_DiacriticSensitivity
title: ISearchCatalogManager::get_DiacriticSensitivity (searchapi.h)
description: Gets a value that indicates whether the catalog is sensitive to diacritics. A diacritic is a mark added to a letter to indicate a special phonetic value or pronunciation.
helpviewer_keywords: ["ISearchCatalogManager interface [search]","get_DiacriticSensitivity method","ISearchCatalogManager.get_DiacriticSensitivity","ISearchCatalogManager::get_DiacriticSensitivity","_search_ISearchCatalogManager_get_DiacriticSensitivity","get_DiacriticSensitivity","get_DiacriticSensitivity method [search]","get_DiacriticSensitivity method [search]","ISearchCatalogManager interface","search._search_ISearchCatalogManager_get_DiacriticSensitivity","searchapi/ISearchCatalogManager::get_DiacriticSensitivity"]
old-location: search\_search_ISearchCatalogManager_get_DiacriticSensitivity.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager\get_diacriticsensitivity.htm
ms.date: 12/05/2018
ms.keywords: ISearchCatalogManager interface [search],get_DiacriticSensitivity method, ISearchCatalogManager.get_DiacriticSensitivity, ISearchCatalogManager::get_DiacriticSensitivity, _search_ISearchCatalogManager_get_DiacriticSensitivity, get_DiacriticSensitivity, get_DiacriticSensitivity method [search], get_DiacriticSensitivity method [search],ISearchCatalogManager interface, search._search_ISearchCatalogManager_get_DiacriticSensitivity, searchapi/ISearchCatalogManager::get_DiacriticSensitivity
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
 - ISearchCatalogManager::get_DiacriticSensitivity
 - searchapi/ISearchCatalogManager::get_DiacriticSensitivity
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
 - ISearchCatalogManager.get_DiacriticSensitivity
---

# ISearchCatalogManager::get_DiacriticSensitivity


## -description

Gets a value that indicates whether the catalog is sensitive to diacritics. A diacritic is a mark added to a letter to indicate a special phonetic value or pronunciation.

## -parameters

### -param pfDiacriticSensitive [out, retval]

Type: <b>BOOL*</b>

Receives a pointer to a Boolean value that indicates whether the catalog is sensitive to diacritics. <b>TRUE</b> if the catalog is sensitive to and recognizes diacritics; otherwise, <b>FALSE</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

