---
UID: NF:tapi3cc.ITACDGroup.get_Name
title: ITACDGroup::get_Name
author: windows-driver-content
description: The get_Name method gets the ACD group name. This string can be a displayable name for the group.
old-location: tapi3\itacdgroup_get_name.htm
old-project: Tapi
ms.assetid: 93e61a42-3e60-4d52-bb19-68842f6947da
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: ITACDGroup interface [TAPI 2.2],get_Name method, ITACDGroup.get_Name, ITACDGroup::get_Name, _tapi3_itacdgroup_get_name, get_Name, get_Name method [TAPI 2.2], get_Name method [TAPI 2.2],ITACDGroup interface, tapi3.itacdgroup_get_name, tapi3cc/ITACDGroup::get_Name
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
-	ITACDGroup.get_Name
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITACDGroup::get_Name


## -description


The 
<b>get_Name</b> method gets the ACD group name. This string can be a displayable name for the group.


## -parameters




### -param ppName [out]

Pointer to <b>BSTR</b> representation of group name.


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
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppName</i> parameter is not a valid pointer.

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
</table>
 




## -remarks



The application must free <i>ppName</i> through 
<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> when the variable is no longer needed.




## -see-also




<a href="https://msdn.microsoft.com/73e23023-5574-4c5a-bdff-cbc7da765a65">ITACDGroup</a>
 

 

