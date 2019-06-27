---
UID: NF:searchapi.ISearchRoot.get_Schedule
title: ISearchRoot::get_Schedule (searchapi.h)
author: windows-sdk-content
description: Not implemented.
old-location: search\_search_ISearchRoot_get_Schedule.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchroot\get_schedule.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISearchRoot interface [search],get_Schedule method, ISearchRoot.get_Schedule, ISearchRoot::get_Schedule, _search_ISearchRoot_get_Schedule, get_Schedule, get_Schedule method [search], get_Schedule method [search],ISearchRoot interface, search._search_ISearchRoot_get_Schedule, searchapi/ISearchRoot::get_Schedule
ms.topic: method
f1_keywords: 
 - "searchapi/ISearchRoot.get_Schedule"
req.header: searchapi.h
req.include-header: Searchapi.h
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
 - searchapi.h
api_name:
 - ISearchRoot.get_Schedule
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISearchRoot::get_Schedule


## -description


Not implemented.


## -parameters




### -param ppszTaskArg [out, retval]

Type: <b>LPWSTR*</b>

Returns the address of a pointer to a null-terminated, Unicode buffer that contains the name of the task.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The CrawlScopeCommandLine code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line 
options for Crawl Scope Manager (CSM) indexing operations.



