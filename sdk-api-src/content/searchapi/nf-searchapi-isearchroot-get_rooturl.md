---
UID: NF:searchapi.ISearchRoot.get_RootURL
title: ISearchRoot::get_RootURL (searchapi.h)
description: Gets the URL of the starting point for this search root.helpviewer_keywords: ["ISearchRoot interface [search]","get_RootURL method","ISearchRoot.get_RootURL","ISearchRoot::get_RootURL","_search_ISearchRoot_get_RootURL","get_RootURL","get_RootURL method [search]","get_RootURL method [search]","ISearchRoot interface","search._search_ISearchRoot_get_RootURL","searchapi/ISearchRoot::get_RootURL"]
old-location: search\_search_ISearchRoot_get_RootURL.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchroot\get_rooturl.htm
ms.date: 12/05/2018
ms.keywords: ISearchRoot interface [search],get_RootURL method, ISearchRoot.get_RootURL, ISearchRoot::get_RootURL, _search_ISearchRoot_get_RootURL, get_RootURL, get_RootURL method [search], get_RootURL method [search],ISearchRoot interface, search._search_ISearchRoot_get_RootURL, searchapi/ISearchRoot::get_RootURL
f1_keywords:
- searchapi/ISearchRoot.get_RootURL
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
- ISearchRoot.get_RootURL
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



Use <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> to free the memory from the returned string.

The CrawlScopeCommandLine code sample, available on <a href="https://code.msdn.microsoft.com/windowssearch">Code Gallery</a> and the <a href="https://msdn.microsoft.com/windowsvista/bb980924.aspx">Windows 7 SDK</a>, demonstrates how to define command line 
options for Crawl Scope Manager (CSM) indexing operations.



