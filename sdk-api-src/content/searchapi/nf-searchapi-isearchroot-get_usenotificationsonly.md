---
UID: NF:searchapi.ISearchRoot.get_UseNotificationsOnly
title: ISearchRoot::get_UseNotificationsOnly
author: windows-driver-content
description: Gets a value that indicates whether this search root should be indexed only by notification and not crawled.
old-location: search\_search_ISearchRoot_get_UseNotificationsOnly.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchroot\get_usenotificationsonly.htm
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: ISearchRoot interface [search],get_UseNotificationsOnly method, ISearchRoot.get_UseNotificationsOnly, ISearchRoot::get_UseNotificationsOnly, _search_ISearchRoot_get_UseNotificationsOnly, get_UseNotificationsOnly, get_UseNotificationsOnly method [search], get_UseNotificationsOnly method [search],ISearchRoot interface, search._search_ISearchRoot_get_UseNotificationsOnly, searchapi/ISearchRoot::get_UseNotificationsOnly
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
req.typenames: ROWSETEVENT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Searchapi.h
api_name:
-	ISearchRoot.get_UseNotificationsOnly
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
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



The CrawlScopeCommandLine code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line 
options for Crawl Scope Manager (CSM) indexing operations.



