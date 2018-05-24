---
UID: NF:searchapi.IEnumSearchScopeRules.Clone
title: IEnumSearchScopeRules::Clone
author: windows-driver-content
description: Creates a copy of this IEnumSearchScopeRules object with the same contents and state as the current one.
old-location: search\_search_IEnumSearchScopeRules_Clone.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\ienumsearchscoperules\clone.htm
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: Clone, Clone method [search], Clone method [search],IEnumSearchScopeRules interface, IEnumSearchScopeRules interface [search],Clone method, IEnumSearchScopeRules.Clone, IEnumSearchScopeRules::Clone, _search_IEnumSearchScopeRules_Clone, search._search_IEnumSearchScopeRules_Clone, searchapi/IEnumSearchScopeRules::Clone
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Searchapi.idl
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
-	IEnumSearchScopeRules.Clone
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IEnumSearchScopeRules::Clone


## -description


Creates a copy of this <a href="https://msdn.microsoft.com/9e285532-8f03-4572-b908-a67abd842268">IEnumSearchScopeRules</a> object with the same contents and state as the current one.


## -parameters




### -param ppenum [out, retval]

Type: <b><a href="https://msdn.microsoft.com/9e285532-8f03-4572-b908-a67abd842268">IEnumSearchScopeRules</a>**</b>

On return, contains a pointer to the cloned <a href="https://msdn.microsoft.com/9e285532-8f03-4572-b908-a67abd842268">IEnumSearchScopeRules</a> object. The calling application must free the new object by calling its <a href="_com_IUnknown_Release">IUnknown::Release</a> method.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>Windows 7 and later</b>: the CrawlScopeCommandLine code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.



