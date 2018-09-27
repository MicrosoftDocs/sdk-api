---
UID: NF:tapi3if.ITDigitsGatheredEvent.get_GatherTermination
title: ITDigitsGatheredEvent::get_GatherTermination
author: windows-sdk-content
description: The get_GatherTermination method gets the reason why the TAPI Server terminated the gathering of digits on the call.
old-location: tapi3\itdigitsgatheredevent_get_gathertermination.htm
tech.root: tapi
ms.assetid: 97c123b9-4497-43f3-b747-660d3f9f5848
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: ITDigitsGatheredEvent interface [TAPI 2.2],get_GatherTermination method, ITDigitsGatheredEvent.get_GatherTermination, ITDigitsGatheredEvent::get_GatherTermination, _tapi3_itdigitsgatheredevent_get_gathertermination, get_GatherTermination, get_GatherTermination method [TAPI 2.2], get_GatherTermination method [TAPI 2.2],ITDigitsGatheredEvent interface, tapi3.itdigitsgatheredevent_get_gathertermination, tapi3if/ITDigitsGatheredEvent::get_GatherTermination
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tapi3if.h
req.include-header: 
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITDigitsGatheredEvent.get_GatherTermination
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITDigitsGatheredEvent::get_GatherTermination


## -description


The 
<b>get_GatherTermination</b> method gets the reason why the TAPI Server terminated the gathering of digits on the call.


## -parameters




### -param pGatherTermination [out]

Pointer to a value from the 
<a href="https://msdn.microsoft.com/781266db-73a3-4202-922f-5c2d13bd3009">TAPI_GATHERTERM</a> enumeration.


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
The <i>pGatherTermination</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/2d710bea-a0fd-492b-81a3-03b741685c91">ITDigitsGatheredEvent</a>
 

 

