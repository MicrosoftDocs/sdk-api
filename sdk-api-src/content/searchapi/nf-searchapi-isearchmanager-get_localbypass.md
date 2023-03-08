---
UID: NF:searchapi.ISearchManager.get_LocalBypass
title: ISearchManager::get_LocalBypass (searchapi.h)
description: Retrieves a value that determines whether the proxy server should be bypassed to find the item or URL.
helpviewer_keywords: ["ISearchManager interface [search]","get_LocalBypass method","ISearchManager.get_LocalBypass","ISearchManager::get_LocalBypass","_search_ISearchManager_get_LocalBypass","get_LocalBypass","get_LocalBypass method [search]","get_LocalBypass method [search]","ISearchManager interface","search._search_ISearchManager_get_LocalBypass","searchapi/ISearchManager::get_LocalBypass"]
old-location: search\_search_ISearchManager_get_LocalBypass.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchmanager\get_localbypass.htm
ms.date: 12/05/2018
ms.keywords: ISearchManager interface [search],get_LocalBypass method, ISearchManager.get_LocalBypass, ISearchManager::get_LocalBypass, _search_ISearchManager_get_LocalBypass, get_LocalBypass, get_LocalBypass method [search], get_LocalBypass method [search],ISearchManager interface, search._search_ISearchManager_get_LocalBypass, searchapi/ISearchManager::get_LocalBypass
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
 - ISearchManager::get_LocalBypass
 - searchapi/ISearchManager::get_LocalBypass
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
 - ISearchManager.get_LocalBypass
---

# ISearchManager::get_LocalBypass


## -description

Retrieves a value that determines whether the proxy server should be bypassed to find the item or URL.

## -parameters

### -param pfLocalBypass [out, retval]

Type: <b>BOOL*</b>

Receives a pointer to a <b>BOOL</b> value that indicates whether to bypass the proxy server to find an item or URL. <b>TRUE</b> to bypass the proxy (for local items); otherwise, <b>FALSE</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Proxy servers are used as a gateway between the local area network (LAN) and the Internet, primarily for security. A proxy server accepts requests for information (on other networks or the Internet) from internal systems such as servers or work stations. The proxy server then forwards the request to the Internet resource, which keeps the address of the requesting system anonymous. When the information returns from the Internet resource, the proxy server routes the information back to the requesting system. For content on the LAN, it is not necessary to go through the proxy server to access your content; this potentially saves time and extra steps.

The value retrieved by this method helps the indexer identify how to work with content that is on a local domain or network. For nonlocal content, going through the proxy server may be appropriate, if not necessary.

The setting to bypass the proxy for local domains is stored in the indexer and is set by calling the <a href="/windows/desktop/api/searchapi/nf-searchapi-isearchmanager-setproxy">ISearchManager::SetProxy</a> method.

Check out the <a href="/windows/win32/search/-search-sample-reindexmatchingurls">ReindexMatchingUrls code sample</a> to see ways to specify which files to re-index and how set it up.