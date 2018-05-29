---
UID: NF:searchapi.IEnumSearchRoots.Next
title: IEnumSearchRoots::Next
author: windows-sdk-content
description: Retrieves the specified number of ISearchRoot elements.
old-location: search\_search_IEnumSearchRoots_Next.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\ienumsearchroots\next.htm
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IEnumSearchRoots interface [search],Next method, IEnumSearchRoots.Next, IEnumSearchRoots::Next, Next, Next method [search], Next method [search],IEnumSearchRoots interface, _search_IEnumSearchRoots_Next, search._search_IEnumSearchRoots_Next, searchapi/IEnumSearchRoots::Next
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
req.typenames: ROWSETEVENT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Searchapi.h
api_name:
-	IEnumSearchRoots.Next
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IEnumSearchRoots::Next


## -description


Retrieves the specified number of <a href="https://msdn.microsoft.com/1df814f4-2403-4a78-bb7d-0e1d98da7265">ISearchRoot</a> elements.
        


## -parameters




### -param celt [in]

Type: <b>ULONG</b>

The number of elements to retrieve.


### -param rgelt [out]

Type: <b><a href="https://msdn.microsoft.com/1df814f4-2403-4a78-bb7d-0e1d98da7265">ISearchRoot</a>**</b>

Retrieves a pointer to an array of <a href="https://msdn.microsoft.com/1df814f4-2403-4a78-bb7d-0e1d98da7265">ISearchRoot</a> elements.


### -param pceltFetched [in, out]

Type: <b>ULONG*</b>

Retrieves a pointer to the actual number of elements retrieved. Can be <b>NULL</b> if <i>celt</i> == 1; otherwise it must not be <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, S_FALSE if there were not enough items left in the enumeration to be returned, or an error value otherwise.




## -remarks



<b>Windows 7 and later</b>: the CrawlScopeCommandLine code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.
        



