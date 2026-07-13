---
UID: NF:searchapi.ISearchManager.put_UserAgent
title: ISearchManager::put_UserAgent (searchapi.h)
description: Sets the user agent string that a user agent passes to website and services to identify itself.
helpviewer_keywords: ["ISearchManager interface [search]","put_UserAgent method","ISearchManager.put_UserAgent","ISearchManager::put_UserAgent","_search_ISearchManager_put_UserAgent","put_UserAgent","put_UserAgent method [search]","put_UserAgent method [search]","ISearchManager interface","search._search_ISearchManager_put_UserAgent","searchapi/ISearchManager::put_UserAgent"]
old-location: search\_search_ISearchManager_put_UserAgent.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchmanager\put_useragent.htm
ms.date: 12/05/2018
ms.keywords: ISearchManager interface [search],put_UserAgent method, ISearchManager.put_UserAgent, ISearchManager::put_UserAgent, _search_ISearchManager_put_UserAgent, put_UserAgent, put_UserAgent method [search], put_UserAgent method [search],ISearchManager interface, search._search_ISearchManager_put_UserAgent, searchapi/ISearchManager::put_UserAgent
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
 - ISearchManager::put_UserAgent
 - searchapi/ISearchManager::put_UserAgent
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
 - ISearchManager.put_UserAgent
---

# ISearchManager::put_UserAgent


## -description

Sets the user agent string that a user agent passes to website and services to identify itself.

## -parameters

### -param pszUserAgent [in]

Type: <b>LPCWSTR</b>

The user agent string identifying the user agent.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A user agent is a client application that accesses the Internet. User agents include web browsers, search engine crawlers, download managers, and so on, and may be associated with a specific protocol such as File Transfer Protocol (FTP) or Hyper Text Transfer Protocol (HTTP).

Each user agent typically has a user agent string, such as "Mozilla/4.0", that it can pass to websites and services to identify itself.

Check out the <a href="/windows/win32/search/-search-sample-reindexmatchingurls">ReindexMatchingUrls code sample</a> to see ways to specify which files to re-index and how set it up.