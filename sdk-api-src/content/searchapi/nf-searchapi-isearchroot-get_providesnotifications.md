---
UID: NF:searchapi.ISearchRoot.get_ProvidesNotifications
title: ISearchRoot::get_ProvidesNotifications (searchapi.h)
description: Gets a value that indicates whether the search engine is notified (by protocol handlers or other applications) about changes to the URLs under the search root.
helpviewer_keywords: ["ISearchRoot interface [search]","get_ProvidesNotifications method","ISearchRoot.get_ProvidesNotifications","ISearchRoot::get_ProvidesNotifications","_search_ISearchRoot_get_ProvidesNotifications","get_ProvidesNotifications","get_ProvidesNotifications method [search]","get_ProvidesNotifications method [search]","ISearchRoot interface","search._search_ISearchRoot_get_ProvidesNotifications","searchapi/ISearchRoot::get_ProvidesNotifications"]
old-location: search\_search_ISearchRoot_get_ProvidesNotifications.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchroot\get_providesnotifications.htm
ms.date: 12/05/2018
ms.keywords: ISearchRoot interface [search],get_ProvidesNotifications method, ISearchRoot.get_ProvidesNotifications, ISearchRoot::get_ProvidesNotifications, _search_ISearchRoot_get_ProvidesNotifications, get_ProvidesNotifications, get_ProvidesNotifications method [search], get_ProvidesNotifications method [search],ISearchRoot interface, search._search_ISearchRoot_get_ProvidesNotifications, searchapi/ISearchRoot::get_ProvidesNotifications
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
 - ISearchRoot::get_ProvidesNotifications
 - searchapi/ISearchRoot::get_ProvidesNotifications
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
 - ISearchRoot.get_ProvidesNotifications
---

# ISearchRoot::get_ProvidesNotifications


## -description

Gets a value that indicates whether the search engine is notified (by protocol handlers or other applications) about changes to the URLs under the search root.

## -parameters

### -param pfProvidesNotifications [out, retval]

Type: <b>BOOL*</b>

On return, points to <b>TRUE</b> if this search root provides notifications; otherwise, <b>FALSE</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The value <b>ISearchRoot::get_ProvidesNotifications</b> returns is not protocol specific.

<b>Windows 7 and later</b>: Check out the <a href="/windows/win32/search/-search-sample-crawlscopecommandline">CrawlScopeCommandLine code sample</a> to see how to define command line 
options for Crawl Scope Manager (CSM) indexing operations.