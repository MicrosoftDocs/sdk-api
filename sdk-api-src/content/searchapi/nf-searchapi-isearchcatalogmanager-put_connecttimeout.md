---
UID: NF:searchapi.ISearchCatalogManager.put_ConnectTimeout
title: ISearchCatalogManager::put_ConnectTimeout (searchapi.h)
description: Sets the connection time-out value in the TIMEOUT_INFO structure, in seconds.
helpviewer_keywords: ["ISearchCatalogManager interface [search]","put_ConnectTimeout method","ISearchCatalogManager.put_ConnectTimeout","ISearchCatalogManager::put_ConnectTimeout","_search_ISearchCatalogManager_put_ConnectTimeout","put_ConnectTimeout","put_ConnectTimeout method [search]","put_ConnectTimeout method [search]","ISearchCatalogManager interface","search._search_ISearchCatalogManager_put_ConnectTimeout","searchapi/ISearchCatalogManager::put_ConnectTimeout"]
old-location: search\_search_ISearchCatalogManager_put_ConnectTimeout.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager\put_connecttimeout.htm
ms.date: 12/05/2018
ms.keywords: ISearchCatalogManager interface [search],put_ConnectTimeout method, ISearchCatalogManager.put_ConnectTimeout, ISearchCatalogManager::put_ConnectTimeout, _search_ISearchCatalogManager_put_ConnectTimeout, put_ConnectTimeout, put_ConnectTimeout method [search], put_ConnectTimeout method [search],ISearchCatalogManager interface, search._search_ISearchCatalogManager_put_ConnectTimeout, searchapi/ISearchCatalogManager::put_ConnectTimeout
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
 - ISearchCatalogManager::put_ConnectTimeout
 - searchapi/ISearchCatalogManager::put_ConnectTimeout
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
 - ISearchCatalogManager.put_ConnectTimeout
---

# ISearchCatalogManager::put_ConnectTimeout


## -description

Sets the connection time-out value in the <a href="/windows/desktop/api/searchapi/ns-searchapi-timeout_info">TIMEOUT_INFO</a> structure, in seconds.

## -parameters

### -param dwConnectTimeout [in]

Type: <b>DWORD</b>

The number of seconds to wait for a connection response.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The indexer expects the first chunk of the document to be received within the connection time-out interval and any subsequent chunks to be received within the data time-out interval. These time-out values help prevent filters and protocol handlers from  failing or causing performance issues.