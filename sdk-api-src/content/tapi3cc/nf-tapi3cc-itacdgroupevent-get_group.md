---
UID: NF:tapi3cc.ITACDGroupEvent.get_Group
title: ITACDGroupEvent::get_Group
author: windows-driver-content
description: The get_Group method gets the ITACDGroup interface pointer for the group on which the event occurred.
old-location: tapi3\itacdgroupevent_get_group.htm
old-project: Tapi
ms.assetid: bbdc94b0-fa46-422a-bffc-32bbd1d49e5a
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: ITACDGroupEvent interface [TAPI 2.2],get_Group method, ITACDGroupEvent.get_Group, ITACDGroupEvent::get_Group, _tapi3_itacdgroupevent_get_group, get_Group, get_Group method [TAPI 2.2], get_Group method [TAPI 2.2],ITACDGroupEvent interface, tapi3.itacdgroupevent_get_group, tapi3cc/ITACDGroupEvent::get_Group
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tapi3cc.h
req.include-header: Tapi3.h
req.target-type: Windows
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
req.typenames: AGENT_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	ITACDGroupEvent.get_Group
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITACDGroupEvent::get_Group


## -description


The 
<b>get_Group</b> method gets the ITACDGroup interface pointer for the group on which the event occurred.


## -parameters




### -param ppGroup [out]

Pointer to 
<a href="https://msdn.microsoft.com/73e23023-5574-4c5a-bdff-cbc7da765a65">ITACDGroup</a> interface on which the event occurred.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppGroup</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/73e23023-5574-4c5a-bdff-cbc7da765a65">ITACDGroup</a> interface returned by <b>ITACDGroupEvent::get_Group</b>. The application must call <b>Release</b> on the 
<b>ITACDGroup</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/73e23023-5574-4c5a-bdff-cbc7da765a65">ITACDGroup</a>



<a href="https://msdn.microsoft.com/5770dca5-cf71-4211-ba9f-0fe7a3bbb614">ITACDGroupEvent</a>
 

 

