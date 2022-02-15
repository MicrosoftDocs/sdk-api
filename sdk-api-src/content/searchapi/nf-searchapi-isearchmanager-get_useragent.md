---
UID: NF:searchapi.ISearchManager.get_UserAgent
title: ISearchManager::get_UserAgent (searchapi.h)
description: Retrieves the user agent string.
helpviewer_keywords: ["ISearchManager interface [search]","get_UserAgent method","ISearchManager.get_UserAgent","ISearchManager::get_UserAgent","_search_ISearchManager_get_UserAgent","get_UserAgent","get_UserAgent method [search]","get_UserAgent method [search]","ISearchManager interface","search._search_ISearchManager_get_UserAgent","searchapi/ISearchManager::get_UserAgent"]
old-location: search\_search_ISearchManager_get_UserAgent.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchmanager\get_useragent.htm
ms.date: 12/05/2018
ms.keywords: ISearchManager interface [search],get_UserAgent method, ISearchManager.get_UserAgent, ISearchManager::get_UserAgent, _search_ISearchManager_get_UserAgent, get_UserAgent, get_UserAgent method [search], get_UserAgent method [search],ISearchManager interface, search._search_ISearchManager_get_UserAgent, searchapi/ISearchManager::get_UserAgent
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
 - ISearchManager::get_UserAgent
 - searchapi/ISearchManager::get_UserAgent
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
 - ISearchManager.get_UserAgent
---

# ISearchManager::get_UserAgent


## -description

Retrieves the user agent string.

## -parameters

### -param ppszUserAgent [out, retval]

Type: <b>LPWSTR*</b>

Receives the address of a pointer to the user agent string.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Check out the <a href="/windows/win32/search/-search-sample-reindexmatchingurls">ReindexMatchingUrls code sample</a> to see ways to specify which files to re-index and how set it up.