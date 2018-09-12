---
UID: NN:searchapi.IUrlAccessor3
title: IUrlAccessor3
author: windows-sdk-content
description: Extends the functionality of the IUrlAccessor2 interface with the IUrlAccessor3::GetImpersonationSidBlobs method to identify user security identifiers (SIDs) for a specified URL.
old-location: search\_search_IUrlAccessor3.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\protocolhandlers\iurlaccessor3\iurlaccessor3.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IUrlAccessor3, IUrlAccessor3 interface [search], IUrlAccessor3 interface [search],described, _search_IUrlAccessor3, search._search_IUrlAccessor3, searchapi/IUrlAccessor3
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Urlaccsdk.idl
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
 - IUrlAccessor3
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Search (WS) 4.0
---

# IUrlAccessor3 interface


## -description


Extends the functionality of the <a href="https://msdn.microsoft.com/en-us/library/Bb231412(v=VS.85).aspx">IUrlAccessor2</a> interface with the <a href="https://msdn.microsoft.com/en-us/library/Cc288228(v=VS.85).aspx">IUrlAccessor3::GetImpersonationSidBlobs</a> method to identify user security identifiers (SIDs) for a specified URL.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUrlAccessor3</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Bb231412(v=VS.85).aspx">IUrlAccessor2</a>. <b>IUrlAccessor3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUrlAccessor3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Cc288228(v=VS.85).aspx">GetImpersonationSidBlobs</a>
</td>
<td align="left" width="63%">
Retrieves an array of user SIDs for a specified URL. This method enables protocol handlers to specify which users can access the file and the search protocol host to impersonate a user in order to index the file.
        

</td>
</tr>
</table> 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb231426(v=VS.85).aspx">IUrlAccessor</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb231412(v=VS.85).aspx">IUrlAccessor2</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Aa965709(v=VS.85).aspx">Search Protocol Handler Error Messages</a>



<a href="https://msdn.microsoft.com/en-us/library/Cc678933(v=VS.85).aspx">The Indexing Process</a>
 

 

