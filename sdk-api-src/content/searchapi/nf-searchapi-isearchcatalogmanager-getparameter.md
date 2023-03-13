---
UID: NF:searchapi.ISearchCatalogManager.GetParameter
title: ISearchCatalogManager::GetParameter (searchapi.h)
description: Not implemented. (ISearchCatalogManager.GetParameter)
helpviewer_keywords: ["GetParameter","GetParameter method [search]","GetParameter method [search]","ISearchCatalogManager interface","ISearchCatalogManager interface [search]","GetParameter method","ISearchCatalogManager.GetParameter","ISearchCatalogManager::GetParameter","_search_ISearchCatalogManager_GetParameter","search._search_ISearchCatalogManager_GetParameter","searchapi/ISearchCatalogManager::GetParameter"]
old-location: search\_search_ISearchCatalogManager_GetParameter.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager\getparameter.htm
ms.date: 12/05/2018
ms.keywords: GetParameter, GetParameter method [search], GetParameter method [search],ISearchCatalogManager interface, ISearchCatalogManager interface [search],GetParameter method, ISearchCatalogManager.GetParameter, ISearchCatalogManager::GetParameter, _search_ISearchCatalogManager_GetParameter, search._search_ISearchCatalogManager_GetParameter, searchapi/ISearchCatalogManager::GetParameter
req.header: searchapi.h
req.include-header: Searchapi.h
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
 - ISearchCatalogManager::GetParameter
 - searchapi/ISearchCatalogManager::GetParameter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - searchapi.h
api_name:
 - ISearchCatalogManager.GetParameter
---

# ISearchCatalogManager::GetParameter


## -description

Not implemented.

## -parameters

### -param pszName [in]

Type: <b>LPCWSTR</b>

The name of the parameter to be retrieved.

### -param ppValue [out, retval]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>**</b>

Receives a pointer to the value of the parameter.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
