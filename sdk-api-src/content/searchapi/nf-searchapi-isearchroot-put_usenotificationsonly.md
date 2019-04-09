---
UID: NF:searchapi.ISearchRoot.put_UseNotificationsOnly
title: ISearchRoot::put_UseNotificationsOnly (searchapi.h)
author: windows-sdk-content
description: Sets a value that indicates whether this search root should be indexed only by notification and not crawled.
old-location: search\_search_ISearchRoot_put_UseNotificationsOnly.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchroot\set_usenotificationsonly.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISearchRoot interface [search],put_UseNotificationsOnly method, ISearchRoot.put_UseNotificationsOnly, ISearchRoot::put_UseNotificationsOnly, _search_ISearchRoot_put_UseNotificationsOnly, put_UseNotificationsOnly, put_UseNotificationsOnly method [search], put_UseNotificationsOnly method [search],ISearchRoot interface, search._search_ISearchRoot_put_UseNotificationsOnly, searchapi/ISearchRoot::put_UseNotificationsOnly
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
 - ISearchRoot.put_UseNotificationsOnly
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For search root URLs in a custom data store or on a remote system, it can be useful to limit the search engine to indexing the URLs only if the store or system has sent notifications that something has changed. This might help to reduce traffic in the store or across the network by avoiding the incremental crawls when the store is unchanged.

The CrawlScopeCommandLine code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line 
options for Crawl Scope Manager (CSM) indexing operations.



