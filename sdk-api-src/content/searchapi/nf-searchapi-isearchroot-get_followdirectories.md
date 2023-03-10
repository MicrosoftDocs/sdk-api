---
UID: NF:searchapi.ISearchRoot.get_FollowDirectories
title: ISearchRoot::get_FollowDirectories (searchapi.h)
description: Gets a BOOL value that indicates whether the search engine follows subdirectories and hierarchical scopes.
helpviewer_keywords: ["ISearchRoot interface [search]","get_FollowDirectories method","ISearchRoot.get_FollowDirectories","ISearchRoot::get_FollowDirectories","_search_ISearchRoot_get_FollowDirectories","get_FollowDirectories","get_FollowDirectories method [search]","get_FollowDirectories method [search]","ISearchRoot interface","search._search_ISearchRoot_get_FollowDirectories","searchapi/ISearchRoot::get_FollowDirectories"]
old-location: search\_search_ISearchRoot_get_FollowDirectories.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchroot\get_followdirectories.htm
ms.date: 12/05/2018
ms.keywords: ISearchRoot interface [search],get_FollowDirectories method, ISearchRoot.get_FollowDirectories, ISearchRoot::get_FollowDirectories, _search_ISearchRoot_get_FollowDirectories, get_FollowDirectories, get_FollowDirectories method [search], get_FollowDirectories method [search],ISearchRoot interface, search._search_ISearchRoot_get_FollowDirectories, searchapi/ISearchRoot::get_FollowDirectories
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
 - ISearchRoot::get_FollowDirectories
 - searchapi/ISearchRoot::get_FollowDirectories
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
 - ISearchRoot.get_FollowDirectories
---

# ISearchRoot::get_FollowDirectories


## -description

Gets a <b>BOOL</b> value that indicates whether the search engine follows subdirectories and hierarchical scopes.

## -parameters

### -param pfFollowDirectories [out, retval]

Type: <b>BOOL*</b>

On return, points to <b>TRUE</b> if the search engine follows subdirectories and hierarchical scopes; otherwise, <b>FALSE</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>Windows 7 and later</b>: Check out the <a href="/windows/win32/search/-search-sample-crawlscopecommandline">CrawlScopeCommandLine code sample</a> to see how to define command line 
options for Crawl Scope Manager (CSM) indexing operations.