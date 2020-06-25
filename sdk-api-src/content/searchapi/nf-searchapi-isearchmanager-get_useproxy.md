---
UID: NF:searchapi.ISearchManager.get_UseProxy
title: ISearchManager::get_UseProxy (searchapi.h)
description: Retrieves the proxy server to be used.
helpviewer_keywords: ["ISearchManager interface [search]","get_UseProxy method","ISearchManager.get_UseProxy","ISearchManager::get_UseProxy","_search_ISearchManager_get_UseProxy","get_UseProxy","get_UseProxy method [search]","get_UseProxy method [search]","ISearchManager interface","search._search_ISearchManager_get_UseProxy","searchapi/ISearchManager::get_UseProxy"]
old-location: search\_search_ISearchManager_get_UseProxy.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchmanager\get_useproxy.htm
ms.date: 12/05/2018
ms.keywords: ISearchManager interface [search],get_UseProxy method, ISearchManager.get_UseProxy, ISearchManager::get_UseProxy, _search_ISearchManager_get_UseProxy, get_UseProxy, get_UseProxy method [search], get_UseProxy method [search],ISearchManager interface, search._search_ISearchManager_get_UseProxy, searchapi/ISearchManager::get_UseProxy
f1_keywords:
- searchapi/ISearchManager.get_UseProxy
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Searchapi.h
api_name:
- ISearchManager.get_UseProxy
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# ISearchManager::get_UseProxy


## -description


Retrieves the proxy server to be used.
        


## -parameters




### -param pUseProxy [out, retval]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/searchapi/ne-searchapi-proxy_access">PROXY_ACCESS</a>*</b>

Receives a pointer to the proxy server to be used.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The ReindexMatchingUrls code sample, available on <a href="https://code.msdn.microsoft.com/windowssearch">Code Gallery</a> and the <a href="https://msdn.microsoft.com/windowsvista/bb980924.aspx">Windows 7 SDK</a>, demonstrates ways to specify which files to re-index and how.



