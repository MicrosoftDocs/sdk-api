---
UID: NF:searchapi.ISearchRoot.put_EnumerationDepth
title: ISearchRoot::put_EnumerationDepth (searchapi.h)
author: windows-sdk-content
description: Sets the enumeration depth for this search root.
old-location: search\_search_ISearchRoot_put_EnumerationDepth.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchroot\put_enumerationdepth.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISearchRoot interface [search],put_EnumerationDepth method, ISearchRoot.put_EnumerationDepth, ISearchRoot::put_EnumerationDepth, _search_ISearchRoot_put_EnumerationDepth, put_EnumerationDepth, put_EnumerationDepth method [search], put_EnumerationDepth method [search],ISearchRoot interface, search._search_ISearchRoot_put_EnumerationDepth, searchapi/ISearchRoot::put_EnumerationDepth
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
 - ISearchRoot.put_EnumerationDepth
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The CrawlScopeCommandLine code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line 
options for Crawl Scope Manager (CSM) indexing operations.



