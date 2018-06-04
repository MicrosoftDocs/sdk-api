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

# ISyncKnowledge2::ContainsKnowledgeForChangeUnit


## -description


Indicates whether the specified knowledge of the specified change unit is known by this knowledge.


## -parameters




### -param pKnowledge [in]

The knowledge object that contains knowledge about <i>pbChangeUnitId</i>.


### -param pbItemId [in]

The ID of the item that contains the change unit to look up.


### -param pbChangeUnitId [in]

The ID of the change unit to look up.


## -returns



The possible return codes include, but are not limited to, the values shown in the following table.

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
This object contains the knowledge known by <i>pKnowledge</i> about <i>pbChangeUnitId</i>.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
This object does not contain the knowledge known by <i>pKnowledge</i> about <i>pbChangeUnitId</i>.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER
</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_ID_FORMAT_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
<i>pbChangeUnitId</i> is not of the format specified by the provider.

</td>
</tr>
</table>
 




## -remarks



Another way to obtain the same result is to pass <i>pbItemId</i> and <i>pbChangeUnitId</i> to the <a href="https://msdn.microsoft.com/67fc3b59-ad82-47a4-9fc6-2d980b9e26fe">ISyncKnowledge::ContainsChangeUnit</a> method of <i>pKnowledge</i>, and then take the resulting projected knowledge and pass it to the <a href="https://msdn.microsoft.com/b6b58390-84be-48ff-a3b9-3b3c83d4f661">ISyncKnowledge::ContainsKnowledge</a> method of this object.





## -see-also




<a href="https://msdn.microsoft.com/cfb08476-7b5d-4953-b723-5160330e57be">ISyncKnowledge Interface</a>



<a href="https://msdn.microsoft.com/1acbae32-8fa6-4c1e-95f6-30aca483c966">ISyncKnowledge2 Interface</a>
 

 

