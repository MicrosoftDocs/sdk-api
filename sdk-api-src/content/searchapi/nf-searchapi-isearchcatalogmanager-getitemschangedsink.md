---
UID: NF:searchapi.ISearchCatalogManager.GetItemsChangedSink
title: ISearchCatalogManager::GetItemsChangedSink (searchapi.h)
description: Gets the change notification sink interface.
helpviewer_keywords: ["GetItemsChangedSink","GetItemsChangedSink method [search]","GetItemsChangedSink method [search]","ISearchCatalogManager interface","ISearchCatalogManager interface [search]","GetItemsChangedSink method","ISearchCatalogManager.GetItemsChangedSink","ISearchCatalogManager::GetItemsChangedSink","_search_ISearchCatalogManager_GetItemsChangedSink","search._search_ISearchCatalogManager_GetItemsChangedSink","searchapi/ISearchCatalogManager::GetItemsChangedSink"]
old-location: search\_search_ISearchCatalogManager_GetItemsChangedSink.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager\getitemschangedsink.htm
ms.date: 12/05/2018
ms.keywords: GetItemsChangedSink, GetItemsChangedSink method [search], GetItemsChangedSink method [search],ISearchCatalogManager interface, ISearchCatalogManager interface [search],GetItemsChangedSink method, ISearchCatalogManager.GetItemsChangedSink, ISearchCatalogManager::GetItemsChangedSink, _search_ISearchCatalogManager_GetItemsChangedSink, search._search_ISearchCatalogManager_GetItemsChangedSink, searchapi/ISearchCatalogManager::GetItemsChangedSink
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
 - ISearchCatalogManager::GetItemsChangedSink
 - searchapi/ISearchCatalogManager::GetItemsChangedSink
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
 - ISearchCatalogManager.GetItemsChangedSink
---

# ISearchCatalogManager::GetItemsChangedSink


## -description

Gets the change notification sink interface.

## -parameters

### -param pISearchNotifyInlineSite [in]

Type: <b><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchnotifyinlinesite">ISearchNotifyInlineSite</a>*</b>

A pointer to your <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchnotifyinlinesite">ISearchNotifyInlineSite</a> interface.

### -param riid [in]

Type: <b>REFIID</b>

The UUID of the <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchitemschangedsink">ISearchItemsChangedSink</a> interface.

### -param ppv [out]

Type: <b>void*</b>

Receives a pointer to the <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchitemschangedsink">ISearchItemsChangedSink</a> interface.

### -param pGUIDCatalogResetSignature [out]

Type: <b>GUID*</b>

Receives a pointer to the GUID representing the catalog reset. If this GUID changes, all notifications must be resent.

### -param pGUIDCheckPointSignature [out]

Type: <b>GUID*</b>

Receives a pointer to the GUID representing a checkpoint.

### -param pdwLastCheckPointNumber [out]

Type: <b>DWORD*</b>

Receives a pointer to the number indicating the last checkpoint to be saved.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.