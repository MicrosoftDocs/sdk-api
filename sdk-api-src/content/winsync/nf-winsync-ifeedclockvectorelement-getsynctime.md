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

# IFeedClockVectorElement::GetSyncTime


## -description


Gets a <a href="https://msdn.microsoft.com/f5e0df02-d016-4eae-9b9b-bfd754ade126">SYNC_TIME</a> value that corresponds to the <b>when</b> value for the item.


## -parameters




### -param pSyncTime [out]

Returns a <a href="https://msdn.microsoft.com/f5e0df02-d016-4eae-9b9b-bfd754ade126">SYNC_TIME</a> value that corresponds to the <b>when</b> value for the item.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>
 




## -remarks



The <a href="https://msdn.microsoft.com/f5e0df02-d016-4eae-9b9b-bfd754ade126">SYNC_TIME</a> structure is a packed date-and-time value that can store years between 1601 and 67136 and times that are accurate to the millisecond.




## -see-also




<a href="https://msdn.microsoft.com/7ffc228f-c4f2-4451-9b23-ec78bf6c8318">IFeedClockVectorElement Interface</a>



<a href="https://msdn.microsoft.com/f5e0df02-d016-4eae-9b9b-bfd754ade126">SYNC_TIME Structure</a>
 

 

