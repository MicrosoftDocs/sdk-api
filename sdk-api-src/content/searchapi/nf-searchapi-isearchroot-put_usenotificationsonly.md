---
UID: NF:searchapi.ISearchRoot.put_UseNotificationsOnly
title: ISearchRoot::put_UseNotificationsOnly (searchapi.h)
description: Sets a value that indicates whether this search root should be indexed only by notification and not crawled.
helpviewer_keywords: ["ISearchRoot interface [search]","put_UseNotificationsOnly method","ISearchRoot.put_UseNotificationsOnly","ISearchRoot::put_UseNotificationsOnly","_search_ISearchRoot_put_UseNotificationsOnly","put_UseNotificationsOnly","put_UseNotificationsOnly method [search]","put_UseNotificationsOnly method [search]","ISearchRoot interface","search._search_ISearchRoot_put_UseNotificationsOnly","searchapi/ISearchRoot::put_UseNotificationsOnly"]
old-location: search\_search_ISearchRoot_put_UseNotificationsOnly.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchroot\set_usenotificationsonly.htm
ms.date: 12/05/2018
ms.keywords: ISearchRoot interface [search],put_UseNotificationsOnly method, ISearchRoot.put_UseNotificationsOnly, ISearchRoot::put_UseNotificationsOnly, _search_ISearchRoot_put_UseNotificationsOnly, put_UseNotificationsOnly, put_UseNotificationsOnly method [search], put_UseNotificationsOnly method [search],ISearchRoot interface, search._search_ISearchRoot_put_UseNotificationsOnly, searchapi/ISearchRoot::put_UseNotificationsOnly
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISearchRoot::put_UseNotificationsOnly
 - searchapi/ISearchRoot::put_UseNotificationsOnly
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
 - ISearchRoot.put_UseNotificationsOnly
---

# ISearchRoot::put_UseNotificationsOnly


## -description

Sets a value that indicates whether this search root should be indexed only by notification and not crawled.

## -parameters

### -param fUseNotificationsOnly [in]

Type: <b>BOOL</b>

<b>TRUE</b> if this search root should be indexed only by notification; otherwise, <b>FALSE</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For search root URLs in a custom data store or on a remote system, it can be useful to limit the search engine to indexing the URLs only if the store or system has sent notifications that something has changed. This might help to reduce traffic in the store or across the network by avoiding the incremental crawls when the store is unchanged.

<b>Windows 7 and later</b>: Check out the <a href="/windows/win32/search/-search-sample-crawlscopecommandline">CrawlScopeCommandLine code sample</a> to see how to define command line options for Crawl Scope Manager (CSM) indexing operations.