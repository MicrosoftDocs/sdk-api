---
UID: NF:searchapi.ISearchRoot.put_ProvidesNotifications
title: ISearchRoot::put_ProvidesNotifications (searchapi.h)
author: windows-sdk-content
description: Sets a value that indicates whether the search engine is notified (by protocol handlers or other applications) about changes to the URLs under the search root.
old-location: search\_search_ISearchRoot_put_ProvidesNotifications.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchroot\put_providesnotifications.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISearchRoot interface [search],put_ProvidesNotifications method, ISearchRoot.put_ProvidesNotifications, ISearchRoot::put_ProvidesNotifications, _search_ISearchRoot_put_ProvidesNotifications, put_ProvidesNotifications, put_ProvidesNotifications method [search], put_ProvidesNotifications method [search],ISearchRoot interface, search._search_ISearchRoot_put_ProvidesNotifications, searchapi/ISearchRoot::put_ProvidesNotifications
ms.topic: method
f1_keywords: ["searchapi/ISearchRoot.put_ProvidesNotifications"]
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
 - ISearchRoot.put_ProvidesNotifications
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISearchRoot::put_ProvidesNotifications


## -description


Sets a value that indicates whether the search engine is notified (by protocol handlers or other applications) about changes to the URLs under the search root.


## -parameters




### -param fProvidesNotifications [in]

Type: <b>BOOL</b>

<b>TRUE</b> if notifications are provided; otherwise, <b>FALSE</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



That value that <b>ISearchRoot::put_ProvidesNotifications</b> sets is not protocol specific.

The CrawlScopeCommandLine code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line 
options for Crawl Scope Manager (CSM) indexing operations.



