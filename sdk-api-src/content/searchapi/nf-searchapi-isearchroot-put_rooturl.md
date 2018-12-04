---
UID: NF:searchapi.ISearchRoot.put_RootURL
title: ISearchRoot::put_RootURL
author: windows-sdk-content
description: Sets the URL of the current search root.
old-location: search\_search_ISearchRoot_put_RootURL.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchroot\put_rooturl.htm
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ISearchRoot interface [search],put_RootURL method, ISearchRoot.put_RootURL, ISearchRoot::put_RootURL, _search_ISearchRoot_put_RootURL, put_RootURL, put_RootURL method [search], put_RootURL method [search],ISearchRoot interface, search._search_ISearchRoot_put_RootURL, searchapi/ISearchRoot::put_RootURL
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
 - ISearchRoot.put_RootURL
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISearchRoot::put_RootURL


## -description


Sets the URL of the current search root.


## -parameters




### -param pszURL [in]

Type: <b>LPCWSTR</b>

Pointer to a null-terminated, Unicode buffer that contains the URL of this search root.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The CrawlScopeCommandLine code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line 
options for Crawl Scope Manager (CSM) indexing operations.



