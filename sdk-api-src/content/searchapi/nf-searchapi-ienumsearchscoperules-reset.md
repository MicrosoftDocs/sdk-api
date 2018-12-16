---
UID: NF:searchapi.IEnumSearchScopeRules.Reset
title: IEnumSearchScopeRules::Reset
author: windows-sdk-content
description: Moves the internal counter to the beginning of the list so that a subsequent call to IEnumSearchScopeRules::Next retrieves from the beginning.
old-location: search\_search_IEnumSearchScopeRules_Reset.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\ienumsearchscoperules\reset.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IEnumSearchScopeRules interface [search],Reset method, IEnumSearchScopeRules.Reset, IEnumSearchScopeRules::Reset, Reset, Reset method [search], Reset method [search],IEnumSearchScopeRules interface, _search_IEnumSearchScopeRules_Reset, search._search_IEnumSearchScopeRules_Reset, searchapi/IEnumSearchScopeRules::Reset
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
 - IEnumSearchScopeRules.Reset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumSearchScopeRules::Reset


## -description


Moves the internal counter to the beginning of the list so that a subsequent call to <a href="https://msdn.microsoft.com/en-us/library/Bb266500(v=VS.85).aspx">IEnumSearchScopeRules::Next</a> retrieves from the beginning.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>Windows 7 and later</b>: the CrawlScopeCommandLine code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.



