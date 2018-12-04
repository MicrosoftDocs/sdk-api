---
UID: NF:searchapi.ISearchRoot.get_IsHierarchical
title: ISearchRoot::get_IsHierarchical
author: windows-sdk-content
description: Gets a value that indicates whether the search is rooted on a hierarchical tree structure.
old-location: search\_search_ISearchRoot_get_IsHierarchical.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchroot\get_ishierarchical.htm
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ISearchRoot interface [search],get_IsHierarchical method, ISearchRoot.get_IsHierarchical, ISearchRoot::get_IsHierarchical, _search_ISearchRoot_get_IsHierarchical, get_IsHierarchical, get_IsHierarchical method [search], get_IsHierarchical method [search],ISearchRoot interface, search._search_ISearchRoot_get_IsHierarchical, searchapi/ISearchRoot::get_IsHierarchical
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
 - ISearchRoot.get_IsHierarchical
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISearchRoot::get_IsHierarchical


## -description


Gets a value that indicates whether the search is rooted on a hierarchical tree structure.
        


## -parameters




### -param pfIsHierarchical [out, retval]

Type: <b>BOOL*</b>

On return, points to <b>TRUE</b> for hierarchical tree structures, and <b>FALSE</b> for other structures such as websites.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The CrawlScopeCommandLine code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line 
options for Crawl Scope Manager (CSM) indexing operations.



