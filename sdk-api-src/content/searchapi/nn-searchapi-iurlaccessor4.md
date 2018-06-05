---
UID: NN:searchapi.IUrlAccessor4
title: IUrlAccessor4
author: windows-sdk-content
description: Extends the functionality of the IUrlAccessor3 interface with the IUrlAccessor4::ShouldIndexItemContent method that identifies whether the content of the item should be indexed.
old-location: search\_search_IUrlAccessor4.htm
old-project: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\protocolhandlers\iurlaccessor4\iurlaccessor4.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
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
-	IUrlAccessor4
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IUrlAccessor4 interface


## -description


Extends the functionality of the <a href="https://msdn.microsoft.com/4e13a780-b264-4baa-a7b5-a5736f2004f8">IUrlAccessor3</a> interface with the <a href="https://msdn.microsoft.com/4b90fce0-9d54-4cd1-969d-7c770b8f8d1f">IUrlAccessor4::ShouldIndexItemContent</a> method that identifies whether the content of the item should be indexed. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUrlAccessor4</b> interface inherits from <a href="https://msdn.microsoft.com/4e13a780-b264-4baa-a7b5-a5736f2004f8">IUrlAccessor3</a>. <b>IUrlAccessor4</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/471388c3-c9f6-49f0-bd28-f683315c0bd3">GetCodePage</a>
</td>
<td align="left" width="63%">

            Gets the code page for properties of the URL item.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/309490fd-eff8-499f-b126-99ac2bae9543">GetDisplayUrl</a>
</td>
<td align="left" width="63%">

            Gets the user-friendly path for the URL item.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9a2fb6f0-d06f-4420-848e-7dae3b84328b">GetImpersonationSidBlobs</a>
</td>
<td align="left" width="63%">

            Retrieves an array of user SIDs for a specified URL. This method enables protocol handlers to specify which users can access the file and the search protocol host to impersonate a user in order to index the file.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/62f237b1-0599-4d9f-bbbb-30bcb90ce14d">IsDocument</a>
</td>
<td align="left" width="63%">
Ascertains whether an item URL is a document or directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4b90fce0-9d54-4cd1-969d-7c770b8f8d1f">ShouldIndexItemContent</a>
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



<a href="https://msdn.microsoft.com/1e6272e7-d9bc-4372-8feb-f96626b88903">IUrlAccessor</a>



<a href="https://msdn.microsoft.com/b4e6eb77-6cc3-48db-8b2a-4f7a3a052e49">IUrlAccessor2</a>



<a href="https://msdn.microsoft.com/4e13a780-b264-4baa-a7b5-a5736f2004f8">IUrlAccessor3</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/cfba12eb-4123-4b57-8311-d4fc8f9f514e">The Indexing Process</a>
 

 

