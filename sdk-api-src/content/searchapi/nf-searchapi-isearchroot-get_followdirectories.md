---
UID: NF:searchapi.ISearchRoot.get_FollowDirectories
title: ISearchRoot::get_FollowDirectories
author: windows-sdk-content
description: Gets a BOOL value that indicates whether the search engine follows subdirectories and hierarchical scopes.
old-location: search\_search_ISearchRoot_get_FollowDirectories.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchroot\get_followdirectories.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ISearchRoot interface [search],get_FollowDirectories method, ISearchRoot.get_FollowDirectories, ISearchRoot::get_FollowDirectories, _search_ISearchRoot_get_FollowDirectories, get_FollowDirectories, get_FollowDirectories method [search], get_FollowDirectories method [search],ISearchRoot interface, search._search_ISearchRoot_get_FollowDirectories, searchapi/ISearchRoot::get_FollowDirectories
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Searchapi.h
api_name:
 - ISearchRoot.get_FollowDirectories
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- searchapi.h
: 
- ISearchRoot.get_FollowDirectories
: 
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The CrawlScopeCommandLine code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line 
options for Crawl Scope Manager (CSM) indexing operations.



