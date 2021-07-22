---
UID: NF:searchapi.ISearchCatalogManager.SetParameter
title: ISearchCatalogManager::SetParameter (searchapi.h)
description: Sets a name/value parameter for the catalog.
helpviewer_keywords: ["ISearchCatalogManager interface [search]","SetParameter method","ISearchCatalogManager.SetParameter","ISearchCatalogManager::SetParameter","SetParameter","SetParameter method [search]","SetParameter method [search]","ISearchCatalogManager interface","_search_ISearchCatalogManager_SetParameter","search._search_ISearchCatalogManager_SetParameter","searchapi/ISearchCatalogManager::SetParameter"]
old-location: search\_search_ISearchCatalogManager_SetParameter.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager\setparameter.htm
ms.date: 12/05/2018
ms.keywords: ISearchCatalogManager interface [search],SetParameter method, ISearchCatalogManager.SetParameter, ISearchCatalogManager::SetParameter, SetParameter, SetParameter method [search], SetParameter method [search],ISearchCatalogManager interface, _search_ISearchCatalogManager_SetParameter, search._search_ISearchCatalogManager_SetParameter, searchapi/ISearchCatalogManager::SetParameter
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
 - ISearchCatalogManager::SetParameter
 - searchapi/ISearchCatalogManager::SetParameter
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
 - ISearchCatalogManager.SetParameter
---

# ISearchCatalogManager::SetParameter


## -description

Sets a name/value parameter for the catalog.

## -parameters

### -param pszName [in]

Type: <b>LPCWSTR</b>

The name of the parameter to change.

### -param pValue [in]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

A pointer to the new value for the parameter.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.