---
UID: NN:searchapi.IEnumSearchRoots
title: IEnumSearchRoots
author: windows-sdk-content
description: Provides methods to enumerate the search roots of a catalog, for example, SystemIndex.
old-location: search\_search_IEnumSearchRoots.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\ienumsearchroots\ienumsearchroots.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IEnumSearchRoots, IEnumSearchRoots interface [search], IEnumSearchRoots interface [search],described, _search_IEnumSearchRoots, search._search_IEnumSearchRoots, searchapi/IEnumSearchRoots
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
 - IEnumSearchRoots
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# IEnumSearchRoots interface


## -description


Provides methods to enumerate the search roots of a catalog, for example, SystemIndex.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumSearchRoots</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumSearchRoots</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumSearchRoots</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266503(v=VS.85).aspx">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the <b>IEnumSearchRoots</b> object with the same contents and state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266505(v=VS.85).aspx">Next</a>
</td>
<td align="left" width="63%">
Retrieves the specified number of <a href="https://msdn.microsoft.com/en-us/library/Bb266469(v=VS.85).aspx">ISearchRoot</a> elements.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266506(v=VS.85).aspx">Reset</a>
</td>
<td align="left" width="63%">
Moves the internal counter to the beginning of the list so a subsequent call to <a href="https://msdn.microsoft.com/en-us/library/Bb266505(v=VS.85).aspx">IEnumSearchRoots::Next</a> retrieves from the beginning.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266507(v=VS.85).aspx">Skip</a>
</td>
<td align="left" width="63%">
Skips the specified number of elements.
        

</td>
</tr>
</table> 


## -remarks



<b>Windows 7 and later</b>: the CrawlScopeCommandLine code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.
        




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb266541(v=VS.85).aspx">Using the Crawl Scope Manager</a>
 

 

