---
UID: NF:searchapi.ISearchRoot.put_FollowDirectories
title: ISearchRoot::put_FollowDirectories (searchapi.h)
description: Sets a BOOL value that indicates whether the search engine should follow subdirectories and hierarchical scopes for this search root.
helpviewer_keywords: ["ISearchRoot interface [search]","put_FollowDirectories method","ISearchRoot.put_FollowDirectories","ISearchRoot::put_FollowDirectories","_search_ISearchRoot_put_FollowDirectories","put_FollowDirectories","put_FollowDirectories method [search]","put_FollowDirectories method [search]","ISearchRoot interface","search._search_ISearchRoot_put_FollowDirectories","searchapi/ISearchRoot::put_FollowDirectories"]
old-location: search\_search_ISearchRoot_put_FollowDirectories.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchroot\put_followdirectories.htm
ms.date: 12/05/2018
ms.keywords: ISearchRoot interface [search],put_FollowDirectories method, ISearchRoot.put_FollowDirectories, ISearchRoot::put_FollowDirectories, _search_ISearchRoot_put_FollowDirectories, put_FollowDirectories, put_FollowDirectories method [search], put_FollowDirectories method [search],ISearchRoot interface, search._search_ISearchRoot_put_FollowDirectories, searchapi/ISearchRoot::put_FollowDirectories
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
 - ISearchRoot::put_FollowDirectories
 - searchapi/ISearchRoot::put_FollowDirectories
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
 - ISearchRoot.put_FollowDirectories
---

# ISearchRoot::put_FollowDirectories


## -description

Sets a <b>BOOL</b> value that indicates whether the search engine should follow subdirectories and hierarchical scopes for this search root.

## -parameters

### -param fFollowDirectories [in]

Type: <b>BOOL</b>

<b>TRUE</b> to follow directories or hierarchical scopes, otherwise <b>FALSE</b>. The default for this value is <b>TRUE</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>Windows 7 and later</b>: Check out the <a href="/windows/win32/search/-search-sample-crawlscopecommandline">CrawlScopeCommandLine code sample</a> to see how to define command line 
options for Crawl Scope Manager (CSM) indexing operations.