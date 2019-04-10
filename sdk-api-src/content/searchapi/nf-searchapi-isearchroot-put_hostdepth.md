---
UID: NF:searchapi.ISearchRoot.put_HostDepth
title: ISearchRoot::put_HostDepth (searchapi.h)
author: windows-sdk-content
description: Sets a value that indicates how far into a host tree to crawl when indexing.
old-location: search\_search_ISearchRoot_put_HostDepth.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchroot\put_hostdepth.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISearchRoot interface [search],put_HostDepth method, ISearchRoot.put_HostDepth, ISearchRoot::put_HostDepth, _search_ISearchRoot_put_HostDepth, put_HostDepth, put_HostDepth method [search], put_HostDepth method [search],ISearchRoot interface, search._search_ISearchRoot_put_HostDepth, searchapi/ISearchRoot::put_HostDepth
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
 - ISearchRoot.put_HostDepth
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The CrawlScopeCommandLine code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line 
options for Crawl Scope Manager (CSM) indexing operations.



