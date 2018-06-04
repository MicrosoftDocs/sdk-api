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

# IInkLineInfo::SetCandidate


## -description



Updates one recognition <i>alternate</i> in the recognition result list, either by replacing an existing alternate, or by adding an alternate to the list.




## -parameters




### -param nCandidateNum [in]

Zero based index of the alternate list entry to set.


### -param strRecogWord [in]

Pointer to the new alternate text.


## -returns



This method can return one of these values.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The <i>nCandidateNum</i> index is out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Could not complete the operation. The recognition result list is not changed.

</td>
</tr>
</table>
 




## -remarks



The <i>candidate</i> list can only be extended by one new entry at a time, at the end of the current list. For example, if the <i>text ink object (tInk)</i> currently has ten recognition results, then setting the <i>nCandidateNum</i> parameter to 10 adds a new result to the text ink object's recognition result list.




## -see-also




<a href="https://msdn.microsoft.com/59005f51-7052-4aef-915d-4c939eecec99">GetCandidate Method</a>



<a href="https://msdn.microsoft.com/58774f49-6af2-4b81-bbd5-709eb694af2d">IInkLineInfo</a>
 

 

