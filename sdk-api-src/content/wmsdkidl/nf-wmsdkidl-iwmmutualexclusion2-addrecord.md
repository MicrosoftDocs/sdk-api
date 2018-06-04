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

# IWMMutualExclusion2::AddRecord


## -description



The <b>AddRecord</b> method adds a record to the mutual exclusion object. Records can hold groups of streams. You can add streams with calls to <a href="https://msdn.microsoft.com/501fae9f-84b3-4025-83bc-ad0bbe47384d">IWMMutualExclusion2::AddStreamForRecord</a>. You can assign a name to a record with a call to <a href="https://msdn.microsoft.com/b288c28c-04bd-49a4-bf11-21d4968772d4">IWMMutualExclusion2::SetName</a>.




## -parameters






## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to allocate memory for the new record.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
There was a problem adding the new record to the collection of records for this mutual exclusion object.

</td>
</tr>
</table>
 




## -remarks



Record numbers, which are used by other methods, are assigned to records sequentially.




## -see-also




<a href="https://msdn.microsoft.com/4a1f468c-2ba5-48a1-b56f-8b62aacf1ccf">IWMMutualExclusion2 Interface</a>



<a href="https://msdn.microsoft.com/501fae9f-84b3-4025-83bc-ad0bbe47384d">IWMMutualExclusion2::AddStreamForRecord</a>



<a href="https://msdn.microsoft.com/74e2825e-2200-4750-bb16-f8cf9f80ab7e">IWMMutualExclusion2::RemoveRecord</a>



<a href="https://msdn.microsoft.com/b288c28c-04bd-49a4-bf11-21d4968772d4">IWMMutualExclusion2::SetName</a>
 

 

