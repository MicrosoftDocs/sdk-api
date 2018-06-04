---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IITResultSet interface


## -description


Use this interface in run-time applications to initialize, build, and obtain information about result sets.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IITResultSet</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IITResultSet</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IITResultSet</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5ca8bdf-4817-498b-833f-519bd734d30a">Add(LPVOID)</a>
</td>
<td align="left" width="63%">
Adds columns to result set, given a header containing pairs of property ID followed by property type.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8320faf1-9cc7-4f17-81eb-721fae9ace5a">Add(PROPID,DWORD,PRIORITY)</a>
</td>
<td align="left" width="63%">
Adds a column to the result set. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ded673f5-72dc-4675-b820-497b8ffa2ad7">Add(PROPID,LPCWSTR,PRIORITY)</a>
</td>
<td align="left" width="63%">
Adds a column to the result set.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5b85831-fc22-4f1e-bf0c-a103ed13d089">Add(PROPID,LPVOID,DWORD,PRIORITY)</a>
</td>
<td align="left" width="63%">
Adds a column to the result set.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj983411">Get</a>
</td>
<td align="left" width="63%">
Gets the property in the specified row and column and fills the given property object.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e76f2028-e1b9-4411-9542-60c54372d8a0">GetRowCount</a>
</td>
<td align="left" width="63%">
Gets the number of rows in a result set.



</td>
</tr>
</table> 

