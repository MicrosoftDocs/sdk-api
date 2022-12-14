---
UID: NF:searchapi.ISearchManager.get_ProxyName
title: ISearchManager::get_ProxyName (searchapi.h)
description: Retrieves the proxy name to be used by the protocol handler.
helpviewer_keywords: ["ISearchManager interface [search]","get_ProxyName method","ISearchManager.get_ProxyName","ISearchManager::get_ProxyName","_search_ISearchManager_get_ProxyName","get_ProxyName","get_ProxyName method [search]","get_ProxyName method [search]","ISearchManager interface","search._search_ISearchManager_get_ProxyName","searchapi/ISearchManager::get_ProxyName"]
old-location: search\_search_ISearchManager_get_ProxyName.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchmanager\get_proxyname.htm
ms.date: 12/05/2018
ms.keywords: ISearchManager interface [search],get_ProxyName method, ISearchManager.get_ProxyName, ISearchManager::get_ProxyName, _search_ISearchManager_get_ProxyName, get_ProxyName, get_ProxyName method [search], get_ProxyName method [search],ISearchManager interface, search._search_ISearchManager_get_ProxyName, searchapi/ISearchManager::get_ProxyName
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
 - ISearchManager::get_ProxyName
 - searchapi/ISearchManager::get_ProxyName
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
 - ISearchManager.get_ProxyName
---

# ISearchManager::get_ProxyName


## -description

Retrieves the proxy name to be used by the protocol handler.

## -parameters

### -param ppszProxyName [out, retval]

Type: <b>LPWSTR*</b>

Receives a pointer to a Unicode string that contains the proxy name.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Check out the <a href="/windows/win32/search/-search-sample-reindexmatchingurls">ReindexMatchingUrls code sample</a> to see ways to specify which files to re-index and how set it up.