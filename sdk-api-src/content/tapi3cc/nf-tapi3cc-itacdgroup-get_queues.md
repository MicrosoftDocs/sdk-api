---
UID: NF:tapi3cc.ITACDGroup.get_Queues
title: ITACDGroup::get_Queues
author: windows-sdk-content
description: The get_Queues method creates a collection of queues associated with the current ACD group. This method is provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the EnumerateQueues method.
old-location: tapi3\itacdgroup_get_queues.htm
old-project: Tapi
ms.assetid: f285fea5-4c08-4d30-8378-0b0aeeea8226
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ITACDGroup interface [TAPI 2.2],get_Queues method, ITACDGroup.get_Queues, ITACDGroup::get_Queues, _tapi3_itacdgroup_get_queues, get_Queues, get_Queues method [TAPI 2.2], get_Queues method [TAPI 2.2],ITACDGroup interface, tapi3.itacdgroup_get_queues, tapi3cc/ITACDGroup::get_Queues
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AGENT_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITACDGroup.get_Queues
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITACDGroup::get_Queues


## -description


The 
<b>get_Queues</b> method creates a collection of queues associated with the current ACD group. This method is provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the 
<a href="https://msdn.microsoft.com/1d9e0dcf-ce43-494f-8adc-845d2856bdd1">EnumerateQueues</a> method.


## -parameters




### -param pVariant [out]

Pointer to <b>VARIANT</b> containing an 
<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a> of 
<a href="https://msdn.microsoft.com/dd1bc6c7-4d4e-4f66-ac5a-7004b85ec023">ITQueue</a> interface pointers (queue objects).


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
The <i>pVariant</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The operation failed because the TAPI 3 DLL timed it out. The timeout interval is two minutes.

</td>
</tr>
</table>
 




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/dd1bc6c7-4d4e-4f66-ac5a-7004b85ec023">ITQueue</a> interface returned by <b>ITACDGroup::get_Queues</b>. The application must call <b>Release</b> on the 
<b>ITQueue</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/1d9e0dcf-ce43-494f-8adc-845d2856bdd1">EnumerateQueues</a>



<a href="https://msdn.microsoft.com/73e23023-5574-4c5a-bdff-cbc7da765a65">ITACDGroup</a>



<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a>



<a href="https://msdn.microsoft.com/dd1bc6c7-4d4e-4f66-ac5a-7004b85ec023">ITQueue</a>
 

 

