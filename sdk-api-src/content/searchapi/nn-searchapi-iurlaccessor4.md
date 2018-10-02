---
UID: NN:searchapi.IUrlAccessor4
title: IUrlAccessor4
author: windows-sdk-content
description: Extends the functionality of the IUrlAccessor3 interface with the IUrlAccessor4::ShouldIndexItemContent method that identifies whether the content of the item should be indexed.
old-location: search\_search_IUrlAccessor4.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\protocolhandlers\iurlaccessor4\iurlaccessor4.htm
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IUrlAccessor4, IUrlAccessor4 interface [search], IUrlAccessor4 interface [search],described, _search_IUrlAccessor4, search._search_IUrlAccessor4, searchapi/IUrlAccessor4
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IUrlAccessor4
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Search (WS) 4.0
---

# IUrlAccessor4 interface


## -description


Extends the functionality of the <a href="https://msdn.microsoft.com/en-us/library/Cc142931(v=VS.85).aspx">IUrlAccessor3</a> interface with the <a href="https://msdn.microsoft.com/en-us/library/Dd183432(v=VS.85).aspx">IUrlAccessor4::ShouldIndexItemContent</a> method that identifies whether the content of the item should be indexed. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUrlAccessor4</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Cc142931(v=VS.85).aspx">IUrlAccessor3</a>. <b>IUrlAccessor4</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUrlAccessor4</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231400(v=VS.85).aspx">GetCodePage</a>
</td>
<td align="left" width="63%">
Gets the code page for properties of the URL item.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231401(v=VS.85).aspx">GetDisplayUrl</a>
</td>
<td align="left" width="63%">
Gets the user-friendly path for the URL item.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Cc288228(v=VS.85).aspx">GetImpersonationSidBlobs</a>
</td>
<td align="left" width="63%">
Retrieves an array of user SIDs for a specified URL. This method enables protocol handlers to specify which users can access the file and the search protocol host to impersonate a user in order to index the file.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231411(v=VS.85).aspx">IsDocument</a>
</td>
<td align="left" width="63%">
Ascertains whether an item URL is a document or directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd183432(v=VS.85).aspx">ShouldIndexItemContent</a>
</td>
<td align="left" width="63%">
Identifies whether the item's content should be indexed. 
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44F10BD2-0CE5-4462-A50B-CBD63EE3B802">ShouldIndexProperty</a>
</td>
<td align="left" width="63%">
Identifies whether a property should be indexed.

</td>
</tr>
</table> 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb231426(v=VS.85).aspx">IUrlAccessor</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb231412(v=VS.85).aspx">IUrlAccessor2</a>



<a href="https://msdn.microsoft.com/en-us/library/Cc142931(v=VS.85).aspx">IUrlAccessor3</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Cc678933(v=VS.85).aspx">The Indexing Process</a>
 

 

