---
UID: NF:searchapi.ISearchRoot.put_EnumerationDepth
title: ISearchRoot::put_EnumerationDepth (searchapi.h)
description: Sets the enumeration depth for this search root.
helpviewer_keywords: ["ISearchRoot interface [search]","put_EnumerationDepth method","ISearchRoot.put_EnumerationDepth","ISearchRoot::put_EnumerationDepth","_search_ISearchRoot_put_EnumerationDepth","put_EnumerationDepth","put_EnumerationDepth method [search]","put_EnumerationDepth method [search]","ISearchRoot interface","search._search_ISearchRoot_put_EnumerationDepth","searchapi/ISearchRoot::put_EnumerationDepth"]
old-location: search\_search_ISearchRoot_put_EnumerationDepth.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchroot\put_enumerationdepth.htm
ms.date: 12/05/2018
ms.keywords: ISearchRoot interface [search],put_EnumerationDepth method, ISearchRoot.put_EnumerationDepth, ISearchRoot::put_EnumerationDepth, _search_ISearchRoot_put_EnumerationDepth, put_EnumerationDepth, put_EnumerationDepth method [search], put_EnumerationDepth method [search],ISearchRoot interface, search._search_ISearchRoot_put_EnumerationDepth, searchapi/ISearchRoot::put_EnumerationDepth
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISearchRoot::put_EnumerationDepth
 - searchapi/ISearchRoot::put_EnumerationDepth
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Searchapi.h
api_name:
 - ISearchRoot.put_EnumerationDepth
---

# ISearchRoot::put_EnumerationDepth


## -description

Sets the enumeration depth for this search root.

## -parameters

### -param dwDepth [in]

Type: <b>DWORD</b>

The depth (number of levels) to enumerate.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>Windows 7 and later</b>: Check out the <a href="/windows/win32/search/-search-sample-crawlscopecommandline">CrawlScopeCommandLine code sample</a> to see how to define command line 
options for Crawl Scope Manager (CSM) indexing operations.