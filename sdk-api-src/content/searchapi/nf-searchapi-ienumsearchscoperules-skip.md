---
UID: NF:searchapi.IEnumSearchScopeRules.Skip
title: IEnumSearchScopeRules::Skip
author: windows-driver-content
description: Skips the specified number of elements.
old-location: search\_search_IEnumSearchScopeRules_Skip.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\ienumsearchscoperules\skip.htm
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IEnumSearchScopeRules interface [search],Skip method, IEnumSearchScopeRules.Skip, IEnumSearchScopeRules::Skip, Skip, Skip method [search], Skip method [search],IEnumSearchScopeRules interface, _search_IEnumSearchScopeRules_Skip, search._search_IEnumSearchScopeRules_Skip, searchapi/IEnumSearchScopeRules::Skip
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
-	IEnumSearchScopeRules.Skip
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IEnumSearchScopeRules::Skip


## -description



          Skips the specified number of elements.
        


## -parameters




### -param celt [in]

Type: <b>ULONG</b>

The number of elements to skip.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, S_FALSE if there were not enough items left in the enumeration to skip, or an error value.




## -remarks



Moves the internal counter a specified number of elements forward so that a subsequent call to <a href="https://msdn.microsoft.com/ef4472f1-348d-4545-8c8f-852a587e8096">IEnumSearchScopeRules::Next</a> starts from that number.

<b>Windows 7 and later</b>: the CrawlScopeCommandLine code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.



