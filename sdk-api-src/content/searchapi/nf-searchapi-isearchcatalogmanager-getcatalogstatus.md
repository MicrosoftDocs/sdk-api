---
UID: NF:searchapi.ISearchCatalogManager.GetCatalogStatus
title: ISearchCatalogManager::GetCatalogStatus (searchapi.h)
description: Gets the status of the catalog.
helpviewer_keywords: ["GetCatalogStatus","GetCatalogStatus method [search]","GetCatalogStatus method [search]","ISearchCatalogManager interface","ISearchCatalogManager interface [search]","GetCatalogStatus method","ISearchCatalogManager.GetCatalogStatus","ISearchCatalogManager::GetCatalogStatus","_search_ISearchCatalogManager_GetCatalogStatus","search._search_ISearchCatalogManager_GetCatalogStatus","searchapi/ISearchCatalogManager::GetCatalogStatus"]
old-location: search\_search_ISearchCatalogManager_GetCatalogStatus.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager\getcatalogstatus.htm
ms.date: 12/05/2018
ms.keywords: GetCatalogStatus, GetCatalogStatus method [search], GetCatalogStatus method [search],ISearchCatalogManager interface, ISearchCatalogManager interface [search],GetCatalogStatus method, ISearchCatalogManager.GetCatalogStatus, ISearchCatalogManager::GetCatalogStatus, _search_ISearchCatalogManager_GetCatalogStatus, search._search_ISearchCatalogManager_GetCatalogStatus, searchapi/ISearchCatalogManager::GetCatalogStatus
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
 - ISearchCatalogManager::GetCatalogStatus
 - searchapi/ISearchCatalogManager::GetCatalogStatus
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
 - ISearchCatalogManager.GetCatalogStatus
---

# ISearchCatalogManager::GetCatalogStatus


## -description

Gets the status of the catalog.

## -parameters

### -param pStatus [out]

Type: <b><a href="/windows/desktop/api/searchapi/ne-searchapi-catalogstatus">CatalogStatus</a>*</b>

Receives a pointer to a value from the <a href="/windows/desktop/api/searchapi/ne-searchapi-catalogstatus">CatalogStatus</a> enumeration. If <i>pStatus</i> is <i>CATALOG_STATUS_PAUSED</i>, further information can be obtained from the <i>pPausedReason</i> parameter.

### -param pPausedReason [out]

Type: <b><a href="/windows/desktop/api/searchapi/ne-searchapi-catalogpausedreason">CatalogPausedReason</a>*</b>

Receives a pointer to a value from the <a href="/windows/desktop/api/searchapi/ne-searchapi-catalogpausedreason">CatalogPausedReason</a> enumeration describing why the catalog is paused. If the catalog status is not <i>CATALOG_STATUS_PAUSED</i>, this parameter receives the value <i>CATALOG_PAUSED_REASON_NONE</i>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.