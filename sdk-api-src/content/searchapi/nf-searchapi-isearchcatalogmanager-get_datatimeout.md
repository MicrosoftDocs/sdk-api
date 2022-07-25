---
UID: NF:searchapi.ISearchCatalogManager.get_DataTimeout
title: ISearchCatalogManager::get_DataTimeout (searchapi.h)
description: Gets the data time-out value, in seconds, for data transactions between the indexer and the search filter host. This value is contained in a TIMEOUT_INFO structure.
helpviewer_keywords: ["ISearchCatalogManager interface [search]","get_DataTimeout method","ISearchCatalogManager.get_DataTimeout","ISearchCatalogManager::get_DataTimeout","_search_ISearchCatalogManager_get_DataTimeout","get_DataTimeout","get_DataTimeout method [search]","get_DataTimeout method [search]","ISearchCatalogManager interface","search._search_ISearchCatalogManager_get_DataTimeout","searchapi/ISearchCatalogManager::get_DataTimeout"]
old-location: search\_search_ISearchCatalogManager_get_DataTimeout.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager\get_datatimeout.htm
ms.date: 12/05/2018
ms.keywords: ISearchCatalogManager interface [search],get_DataTimeout method, ISearchCatalogManager.get_DataTimeout, ISearchCatalogManager::get_DataTimeout, _search_ISearchCatalogManager_get_DataTimeout, get_DataTimeout, get_DataTimeout method [search], get_DataTimeout method [search],ISearchCatalogManager interface, search._search_ISearchCatalogManager_get_DataTimeout, searchapi/ISearchCatalogManager::get_DataTimeout
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
 - ISearchCatalogManager::get_DataTimeout
 - searchapi/ISearchCatalogManager::get_DataTimeout
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
 - ISearchCatalogManager.get_DataTimeout
---

# ISearchCatalogManager::get_DataTimeout


## -description

Gets the data time-out value, in seconds, for data transactions between the indexer and the search  filter host. This value is contained in a <a href="/windows/desktop/api/searchapi/ns-searchapi-timeout_info">TIMEOUT_INFO</a> structure.

## -parameters

### -param pdwDataTimeout [out, retval]

Type: <b>DWORD*</b>

Receives a pointer to the <a href="/windows/desktop/api/searchapi/ns-searchapi-timeout_info">TIMEOUT_INFO</a> value for data transactions (the amount of time to wait for a data transaction).

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The indexer expects the first chunk of a document to be received within the connection time-out interval and any subsequent chunks to be received within the data time-out interval. These time-out values help prevent filters and protocol handlers from  failing or causing performance issues.