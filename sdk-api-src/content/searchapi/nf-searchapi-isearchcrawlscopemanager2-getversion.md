---
UID: NF:searchapi.ISearchCrawlScopeManager2.GetVersion
title: ISearchCrawlScopeManager2::GetVersion (searchapi.h)
description: Causes file mapping to be mapped into the address space of the calling process, and informs clients if the state of the Crawl Scope Manager (CSM) has changed.
helpviewer_keywords: ["GetVersion","GetVersion method [search]","GetVersion method [search]","ISearchCrawlScopeManager2 interface","ISearchCrawlScopeManager2 interface [search]","GetVersion method","ISearchCrawlScopeManager2.GetVersion","ISearchCrawlScopeManager2::GetVersion","_search_ISearchCrawlScopeManager2_GetVersion","search._search_ISearchCrawlScopeManager2_GetVersion","searchapi/ISearchCrawlScopeManager2::GetVersion"]
old-location: search\_search_ISearchCrawlScopeManager2_GetVersion.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\crawlscope\isearchcrawlscopemanager2\getversion.htm
ms.date: 12/05/2018
ms.keywords: GetVersion, GetVersion method [search], GetVersion method [search],ISearchCrawlScopeManager2 interface, ISearchCrawlScopeManager2 interface [search],GetVersion method, ISearchCrawlScopeManager2.GetVersion, ISearchCrawlScopeManager2::GetVersion, _search_ISearchCrawlScopeManager2_GetVersion, search._search_ISearchCrawlScopeManager2_GetVersion, searchapi/ISearchCrawlScopeManager2::GetVersion
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Searchcrawlscopemanager.idl
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
 - ISearchCrawlScopeManager2::GetVersion
 - searchapi/ISearchCrawlScopeManager2::GetVersion
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
 - ISearchCrawlScopeManager2.GetVersion
---

# ISearchCrawlScopeManager2::GetVersion


## -description

Causes file mapping to be mapped into the address space of the calling process, and informs clients if the state of the Crawl Scope Manager (CSM) has changed.

## -parameters

### -param plVersion [out]

Type: <b>LONG**</b>

Receives a pointer to the address of a memory mapped file that contains the crawl scope version.

### -param phFileMapping [out]

Type: <b>HANDLE*</b>

Receives a pointer to the handle of the file mapping object, with read-only access, that was used to create the memory mapped file that contains the crawl scope version.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The version number that is retrieved is always current, and changes as the state of the CSM, such as whether additions or removals were made to the crawl scope, for example. Hence, <b>ISearchCrawlScopeManager2::GetVersion</b> needs to be called only once, because the current version always remains available through the retrieved pointer.

<b>ISearchCrawlScopeManager2::GetVersion</b> does not result in a cross-process call. If the method succeeds, then the client must perform the following actions to destroy all file views in its address space, and then close the file mapping object's handle and the file on disk:

<ul>
<li>Call <b>UnmapViewOfFile</b> using the pointer of the memory-mapped file provided by <i>plVersion</i></li>
<li>Call <b>CloseHandle</b> using the handle of the file mapping object</li>
</ul>
The client must perform these steps when finished using the memory mapped file, to prevent memory leaks.

<b>Windows 7 and later</b>: Check out the <a href="/windows/win32/search/-search-sample-crawlscopecommandline">CrawlScopeCommandLine code sample</a> to see how to define command line options for Crawl Scope Manager (CSM) indexing operations.