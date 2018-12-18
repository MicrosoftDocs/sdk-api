---
UID: NF:searchapi.ISearchRoot.get_RootURL
title: ISearchRoot::get_RootURL
author: windows-sdk-content
description: Gets the URL of the starting point for this search root.
old-location: search\_search_ISearchRoot_get_RootURL.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchroot\get_rooturl.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISearchRoot interface [search],get_RootURL method, ISearchRoot.get_RootURL, ISearchRoot::get_RootURL, _search_ISearchRoot_get_RootURL, get_RootURL, get_RootURL method [search], get_RootURL method [search],ISearchRoot interface, search._search_ISearchRoot_get_RootURL, searchapi/ISearchRoot::get_RootURL
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
 - ISearchRoot.get_RootURL
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISearchRoot::get_RootURL


## -description


Gets the URL of the starting point for this search root.
        


## -parameters




### -param ppszURL [out, retval]

Type: <b>LPWSTR*</b>

A null-terminated, Unicode buffer that contains the URL.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Use <a href="https://msdn.microsoft.com/en-us/library/ms680722(v=VS.85).aspx">CoTaskMemFree</a> to free the memory from the returned string.

The CrawlScopeCommandLine code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line 
options for Crawl Scope Manager (CSM) indexing operations.



