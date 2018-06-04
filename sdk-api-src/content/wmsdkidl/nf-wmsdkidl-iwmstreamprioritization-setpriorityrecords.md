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

# IWMStreamPrioritization::SetPriorityRecords


## -description



The <b>SetPriorityRecords</b> method assigns the members of an array as the stream priority list in the stream prioritization object.




## -parameters




### -param pRecordArray [in]

Pointer to an array of <a href="https://msdn.microsoft.com/43c9370c-cd43-4dd0-8258-d6dbdb98f1de">WM_STREAM_PRIORITY_RECORD</a> structures.


### -param cRecords [in]

Count of records.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>cRecords</i> specifies a record count greater than zero, but <i>pRecordArray</i> is <b>NULL</b>.

OR

One of the array rules has been broken (see the Remarks section).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method is unable to allocate the memory required to store the array in the stream prioritization object.

</td>
</tr>
</table>
 




## -remarks



Valid arrays contain no duplicate stream numbers. Streams are listed in the array in descending priority order. Any stream that is designated as mandatory must occur in the array before any entries that are optional. If any of these rules are broken, <b>SetPriorityRecords</b> will return E_INVALIDARG.

<b>SetPriorityRecords</b> overwrites an existing stream priority array if there is one. You can clear the array by passing zero for <i>cRecords</i>.

This method does not verify that the streams specified are valid for the profile.




## -see-also




<a href="https://msdn.microsoft.com/ef8ae275-c36a-492c-b57c-d640044ede93">IWMStreamPrioritization Interface</a>



<a href="https://msdn.microsoft.com/50b105c7-1e4f-435c-8bb6-643ea4d065bb">IWMStreamPrioritization::GetPriorityRecords</a>



<a href="https://msdn.microsoft.com/43c9370c-cd43-4dd0-8258-d6dbdb98f1de">WM_STREAM_PRIORITY_RECORD</a>
 

 

