---
UID: NF:searchapi.ISearchRoot.put_HostDepth
title: ISearchRoot::put_HostDepth (searchapi.h)
description: Sets a value that indicates how far into a host tree to crawl when indexing.
helpviewer_keywords: ["ISearchRoot interface [search]","put_HostDepth method","ISearchRoot.put_HostDepth","ISearchRoot::put_HostDepth","_search_ISearchRoot_put_HostDepth","put_HostDepth","put_HostDepth method [search]","put_HostDepth method [search]","ISearchRoot interface","search._search_ISearchRoot_put_HostDepth","searchapi/ISearchRoot::put_HostDepth"]
old-location: search\_search_ISearchRoot_put_HostDepth.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchroot\put_hostdepth.htm
ms.date: 12/05/2018
ms.keywords: ISearchRoot interface [search],put_HostDepth method, ISearchRoot.put_HostDepth, ISearchRoot::put_HostDepth, _search_ISearchRoot_put_HostDepth, put_HostDepth, put_HostDepth method [search], put_HostDepth method [search],ISearchRoot interface, search._search_ISearchRoot_put_HostDepth, searchapi/ISearchRoot::put_HostDepth
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
 - ISearchRoot::put_HostDepth
 - searchapi/ISearchRoot::put_HostDepth
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
 - ISearchRoot.put_HostDepth
---

# ISearchRoot::put_HostDepth


## -description

<p class="CCE_Message">[<b>put_HostDepth</b> may be altered or unavailable in subsequent versions of the operating system or product.]

Sets a value that indicates how far into a host tree to crawl when indexing.

## -parameters

### -param dwDepth [in]

Type: <b>DWORD</b>

The depth (number of levels) to crawl a host tree.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>Windows 7 and later</b>: Check out the <a href="/windows/win32/search/-search-sample-crawlscopecommandline">CrawlScopeCommandLine code sample</a> to see how to define command line 
options for Crawl Scope Manager (CSM) indexing operations.