---
UID: NF:searchapi.ISearchCatalogManager.RegisterViewForNotification
title: ISearchCatalogManager::RegisterViewForNotification (searchapi.h)
description: Not implemented. (ISearchCatalogManager.RegisterViewForNotification)
helpviewer_keywords: ["ISearchCatalogManager interface [search]","RegisterViewForNotification method","ISearchCatalogManager.RegisterViewForNotification","ISearchCatalogManager::RegisterViewForNotification","RegisterViewForNotification","RegisterViewForNotification method [search]","RegisterViewForNotification method [search]","ISearchCatalogManager interface","_search_ISearchCatalogManager_RegisterViewForNotification","search._search_ISearchCatalogManager_RegisterViewForNotification","searchapi/ISearchCatalogManager::RegisterViewForNotification"]
old-location: search\_search_ISearchCatalogManager_RegisterViewForNotification.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager\registerviewfornotification.htm
ms.date: 12/05/2018
ms.keywords: ISearchCatalogManager interface [search],RegisterViewForNotification method, ISearchCatalogManager.RegisterViewForNotification, ISearchCatalogManager::RegisterViewForNotification, RegisterViewForNotification, RegisterViewForNotification method [search], RegisterViewForNotification method [search],ISearchCatalogManager interface, _search_ISearchCatalogManager_RegisterViewForNotification, search._search_ISearchCatalogManager_RegisterViewForNotification, searchapi/ISearchCatalogManager::RegisterViewForNotification
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
 - ISearchCatalogManager::RegisterViewForNotification
 - searchapi/ISearchCatalogManager::RegisterViewForNotification
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
 - ISearchCatalogManager.RegisterViewForNotification
---

# ISearchCatalogManager::RegisterViewForNotification


## -description

Not implemented.

## -parameters

### -param pszView [in]

Type: <b>LPCWSTR</b>

A pointer to the name of the view.

### -param pViewChangedSink [in]

Type: <b><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchviewchangedsink">ISearchViewChangedSink</a>*</b>

Pointer to the <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchviewchangedsink">ISearchViewChangedSink</a> object to receive notifications.

### -param pdwCookie [out]

Type: <b>DWORD*</b>

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
