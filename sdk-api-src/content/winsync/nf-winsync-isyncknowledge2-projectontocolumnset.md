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

# ISyncKnowledge2::ProjectOntoColumnSet


## -description


Returns the knowledge for the specified set of change units for all the items that are contained in this object.


## -parameters




### -param ppColumns [in]

The set of change unit IDs to look up.


### -param count [in]

The number of change unit IDs that are contained in <i>ppColumns</i>.


### -param ppiKnowledgeOut [out]

A knowledge object that contains only the change units that are specified by <i>ppColumns</i> for all items contained in this object.


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
<i>count</i> is zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
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
The format of the change unit IDs that is contained in <i>ppColumns</i> is not of the format that the format schema of the provider specified.

</td>
</tr>
</table>
 




## -remarks



<b>ProjectOntoColumnSet</b> differs from <a href="https://msdn.microsoft.com/3c09284f-9866-49a4-adeb-561af3351ada">ISyncKnowledge::ProjectOntoChangeUnit</a>. <b>ProjectOntoColumnSet</b> returns a knowledge object that contains information about the specified set of change units for all the items that are contained in the knowledge object. <b>ProjectOntoChangeUnit</b> returns a knowledge object that contains information about a single change unit that is contained in a single item.





## -see-also




<a href="https://msdn.microsoft.com/cfb08476-7b5d-4953-b723-5160330e57be">ISyncKnowledge Interface</a>



<a href="https://msdn.microsoft.com/1acbae32-8fa6-4c1e-95f6-30aca483c966">ISyncKnowledge2 Interface</a>
 

 

