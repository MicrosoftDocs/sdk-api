---
UID: NF:searchapi.ISearchManager.SetProxy
title: ISearchManager::SetProxy (searchapi.h)
description: Stores information in the indexer that determines how the indexer will work and communicate with a proxy server.
helpviewer_keywords: ["ISearchManager interface [search]","SetProxy method","ISearchManager.SetProxy","ISearchManager::SetProxy","SetProxy","SetProxy method [search]","SetProxy method [search]","ISearchManager interface","_search_ISearchManager_SetProxy","search._search_ISearchManager_SetProxy","searchapi/ISearchManager::SetProxy"]
old-location: search\_search_ISearchManager_SetProxy.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchmanager\setproxy.htm
ms.date: 12/05/2018
ms.keywords: ISearchManager interface [search],SetProxy method, ISearchManager.SetProxy, ISearchManager::SetProxy, SetProxy, SetProxy method [search], SetProxy method [search],ISearchManager interface, _search_ISearchManager_SetProxy, search._search_ISearchManager_SetProxy, searchapi/ISearchManager::SetProxy
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Searchadmin.idl
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
 - ISearchManager::SetProxy
 - searchapi/ISearchManager::SetProxy
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
 - ISearchManager.SetProxy
---

# ISearchManager::SetProxy


## -description

Stores information in the indexer that determines how the indexer will work and communicate with a proxy server.

## -parameters

### -param sUseProxy [in]

Type: <b><a href="/windows/desktop/api/searchapi/ne-searchapi-proxy_access">PROXY_ACCESS</a></b>

Sets whether and how to use a proxy, using one of the values enumerated in <a href="/windows/desktop/api/searchapi/ne-searchapi-proxy_access">PROXY_ACCESS</a>.

### -param fLocalByPassProxy [in]

Type: <b>BOOL</b>

Sets whether the proxy server should be bypassed for local items and URLs.

### -param dwPortNumber [in]

Type: <b>DWORD</b>

Sets the port number that the index will use to talk to the proxy server.

### -param pszProxyName [in]

Type: <b>LPCWSTR</b>

A null-terminated Unicode string containing the name of the proxy server to use.

### -param pszByPassList [in]

Type: <b>LPCWSTR</b>

A null-terminated Unicode string containing a comma-delimited list of items that are considered local by the indexer and are not to be accessed through a proxy server.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Check out the <a href="/windows/win32/search/-search-sample-reindexmatchingurls">ReindexMatchingUrls code sample</a> to see ways to specify which files to re-index and how set it up.