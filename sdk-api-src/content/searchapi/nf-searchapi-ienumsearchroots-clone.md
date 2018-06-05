---
UID: NF:searchapi.IEnumSearchRoots.Clone
title: IEnumSearchRoots::Clone
author: windows-sdk-content
description: Creates a copy of the IEnumSearchRoots object with the same contents and state as the current one.
old-location: search\_search_IEnumSearchRoots_Clone.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\ienumsearchroots\clone.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: Clone, Clone method [search], Clone method [search],IEnumSearchRoots interface, IEnumSearchRoots interface [search],Clone method, IEnumSearchRoots.Clone, IEnumSearchRoots::Clone, _search_IEnumSearchRoots_Clone, search._search_IEnumSearchRoots_Clone, searchapi/IEnumSearchRoots::Clone
ms.prod: windows
ms.technology: windows-sdk
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
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: ROWSETEVENT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Searchapi.h
api_name:
-	IEnumSearchRoots.Clone
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IEnumSearchRoots::Clone


## -description


Creates a copy of the <a href="https://msdn.microsoft.com/4fac0cf0-165d-45f2-8e63-02f0c8eae431">IEnumSearchRoots</a> object with the same contents and state as the current one.


## -parameters




### -param ppenum [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4fac0cf0-165d-45f2-8e63-02f0c8eae431">IEnumSearchRoots</a>**</b>

Returns a pointer to the new <a href="https://msdn.microsoft.com/4fac0cf0-165d-45f2-8e63-02f0c8eae431">IEnumSearchRoots</a> object. The calling application must free the new object by calling its <a href="_com_IUnknown_Release">IUnknown::Release</a> method.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>Windows 7 and later</b>: the CrawlScopeCommandLine code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.
        



