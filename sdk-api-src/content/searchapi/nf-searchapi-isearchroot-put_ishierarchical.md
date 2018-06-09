---
UID: NF:searchapi.ISearchRoot.put_IsHierarchical
title: ISearchRoot::put_IsHierarchical
author: windows-sdk-content
description: Sets a value that indicates whether the search is rooted on a hierarchical tree structure.
old-location: search\_search_ISearchRoot_put_IsHierarchical.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchroot\put_ishierarchical.htm
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ISearchRoot interface [search],put_IsHierarchical method, ISearchRoot.put_IsHierarchical, ISearchRoot::put_IsHierarchical, _search_ISearchRoot_put_IsHierarchical, put_IsHierarchical, put_IsHierarchical method [search], put_IsHierarchical method [search],ISearchRoot interface, search._search_ISearchRoot_put_IsHierarchical, searchapi/ISearchRoot::put_IsHierarchical
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: ROWSETEVENT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Searchapi.h
api_name:
 - ISearchRoot.put_IsHierarchical
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISearchRoot::put_IsHierarchical


## -description


Sets a value that indicates whether the search is rooted on a hierarchical tree structure.


## -parameters




### -param fIsHierarchical [in]

Type: <b>BOOL</b>

<b>TRUE</b> for hierarchical tree structures, <b>FALSE</b> for non-hierarchical systems such as websites.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The CrawlScopeCommandLine code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line 
options for Crawl Scope Manager (CSM) indexing operations.



