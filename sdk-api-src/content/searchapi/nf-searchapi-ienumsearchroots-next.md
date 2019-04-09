---
UID: NF:searchapi.IEnumSearchRoots.Next
title: IEnumSearchRoots::Next (searchapi.h)
author: windows-sdk-content
description: Retrieves the specified number of ISearchRoot elements.
old-location: search\_search_IEnumSearchRoots_Next.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\ienumsearchroots\next.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumSearchRoots interface [search],Next method, IEnumSearchRoots.Next, IEnumSearchRoots::Next, Next, Next method [search], Next method [search],IEnumSearchRoots interface, _search_IEnumSearchRoots_Next, search._search_IEnumSearchRoots_Next, searchapi/IEnumSearchRoots::Next
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
 - IEnumSearchRoots.Next
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# IEnumSearchRoots::Next


## -description


Retrieves the specified number of <a href="https://msdn.microsoft.com/en-us/library/Bb266469(v=VS.85).aspx">ISearchRoot</a> elements.
        


## -parameters




### -param celt [in]

Type: <b>ULONG</b>

The number of elements to retrieve.


### -param rgelt [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb266469(v=VS.85).aspx">ISearchRoot</a>**</b>

Retrieves a pointer to an array of <a href="https://msdn.microsoft.com/en-us/library/Bb266469(v=VS.85).aspx">ISearchRoot</a> elements.


### -param pceltFetched [in, out]

Type: <b>ULONG*</b>

Retrieves a pointer to the actual number of elements retrieved. Can be <b>NULL</b> if <i>celt</i> == 1; otherwise it must not be <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, S_FALSE if there were not enough items left in the enumeration to be returned, or an error value otherwise.




## -remarks



<b>Windows 7 and later</b>: the CrawlScopeCommandLine code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.
        



