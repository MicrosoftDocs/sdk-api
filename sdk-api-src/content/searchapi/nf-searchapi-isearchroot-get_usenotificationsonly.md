---
UID: NF:searchapi.ISearchRoot.get_UseNotificationsOnly
title: ISearchRoot::get_UseNotificationsOnly (searchapi.h)
description: Gets a value that indicates whether this search root should be indexed only by notification and not crawled.
helpviewer_keywords: ["ISearchRoot interface [search]","get_UseNotificationsOnly method","ISearchRoot.get_UseNotificationsOnly","ISearchRoot::get_UseNotificationsOnly","_search_ISearchRoot_get_UseNotificationsOnly","get_UseNotificationsOnly","get_UseNotificationsOnly method [search]","get_UseNotificationsOnly method [search]","ISearchRoot interface","search._search_ISearchRoot_get_UseNotificationsOnly","searchapi/ISearchRoot::get_UseNotificationsOnly"]
old-location: search\_search_ISearchRoot_get_UseNotificationsOnly.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchroot\get_usenotificationsonly.htm
ms.date: 12/05/2018
ms.keywords: ISearchRoot interface [search],get_UseNotificationsOnly method, ISearchRoot.get_UseNotificationsOnly, ISearchRoot::get_UseNotificationsOnly, _search_ISearchRoot_get_UseNotificationsOnly, get_UseNotificationsOnly, get_UseNotificationsOnly method [search], get_UseNotificationsOnly method [search],ISearchRoot interface, search._search_ISearchRoot_get_UseNotificationsOnly, searchapi/ISearchRoot::get_UseNotificationsOnly
f1_keywords:
- searchapi/ISearchRoot.get_UseNotificationsOnly
dev_langs:
- c++
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
- ISearchRoot.get_UseNotificationsOnly
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISearchRoot::get_UseNotificationsOnly


## -description


Gets a value that indicates whether this search root should be indexed only by notification and not crawled.


## -parameters




### -param pfUseNotificationsOnly [out, retval]

Type: <b>BOOL*</b>

On return, points to <b>TRUE</b> if this search root should be indexed only by notification; otherwise, <b>FALSE</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The CrawlScopeCommandLine code sample, available on <a href="https://code.msdn.microsoft.com/windowssearch">Code Gallery</a> and the <a href="https://msdn.microsoft.com/windowsvista/bb980924.aspx">Windows 7 SDK</a>, demonstrates how to define command line 
options for Crawl Scope Manager (CSM) indexing operations.



