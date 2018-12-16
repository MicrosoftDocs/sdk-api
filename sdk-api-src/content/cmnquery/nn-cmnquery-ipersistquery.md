---
UID: NN:cmnquery.IPersistQuery
title: IPersistQuery
author: windows-sdk-content
description: Used to store and retrieve query parameters to and from persistent storage.
old-location: ad\ipersistquery.htm
tech.root: ad
ms.assetid: 9d90f119-3d10-4f06-bed4-5ffab9ae14a4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IPersistQuery, IPersistQuery interface [Active Directory], IPersistQuery interface [Active Directory],described, _glines_ipersistquery, ad.ipersistquery, cmnquery/IPersistQuery
ms.topic: interface
req.header: cmnquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Dsquery.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dsquery.dll
api_name:
 - IPersistQuery
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPersistQuery interface


## -description


The <b>IPersistQuery</b> interface is used to store and retrieve query parameters to and from persistent storage.This storage pertains to the query parameters, not the results of a query. A pointer to this interface is provided to a query form extension in the <a href="https://msdn.microsoft.com/f01586dd-4ed3-45af-9e25-a596a693313d">CQPM_PERSIST</a> message. An application can also provide its own  <b>IPersistQuery</b> implementation by passing a pointer to this interface to the query handler in the <b>pPersistQuery</b> member of the <a href="https://msdn.microsoft.com/en-us/library/ms677622(v=VS.85).aspx">OPENQUERYWINDOW</a> structure when <a href="https://msdn.microsoft.com/604c4d7a-1f85-4e5b-9879-be502c5c7bff">ICommonQuery::OpenQueryWindow</a> is called.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPersistQuery</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/ms688695(v=VS.85).aspx">IPersist</a>. <b>IPersistQuery</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPersistQuery</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ce97afa-6d59-446c-9af2-595ec18db2b7">Clear</a>
</td>
<td align="left" width="63%">
Empties the contents of the query store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e7db105f-d331-4048-8d75-e85af94a5c54">ReadInt</a>
</td>
<td align="left" width="63%">
Reads an integer value from the query  store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5d96234f-080e-49c6-ae31-c4eb672ecf04">ReadString</a>
</td>
<td align="left" width="63%">
Reads a string from the query store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/47d1b733-7e37-42f8-b344-909a6e48b381">ReadStruct</a>
</td>
<td align="left" width="63%">
Reads a structure from the query store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f68865a-dd9f-4428-9cbc-f998f0f1f4a7">WriteInt</a>
</td>
<td align="left" width="63%">
Writes an integer value to the query store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6bf8499a-6b3a-4786-8d42-67ab4e1a40c0">WriteString</a>
</td>
<td align="left" width="63%">
Writes a string to the query store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c0acd6c7-96ee-4650-9cfc-3bad4fdffdcc">WriteStruct</a>
</td>
<td align="left" width="63%">
Writes a structure to the query store.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/f01586dd-4ed3-45af-9e25-a596a693313d">CQPM_PERSIST</a>



<a href="https://msdn.microsoft.com/f53d4425-5496-45f8-a09b-f163b63a29c8">Display Interfaces in Active Directory Domain Services</a>



<a href="https://msdn.microsoft.com/604c4d7a-1f85-4e5b-9879-be502c5c7bff">ICommonQuery::OpenQueryWindow</a>



<a href="https://msdn.microsoft.com/en-us/library/ms688695(v=VS.85).aspx">IPersist</a>



<a href="https://msdn.microsoft.com/en-us/library/ms677622(v=VS.85).aspx">OPENQUERYWINDOW</a>
 

 

