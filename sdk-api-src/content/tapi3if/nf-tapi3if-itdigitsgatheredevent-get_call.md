---
UID: NF:tapi3if.ITDigitsGatheredEvent.get_Call
title: ITDigitsGatheredEvent::get_Call
author: windows-sdk-content
description: The get_Call method gets a pointer to the call information interface for the call object on which the event occurred.
old-location: tapi3\itdigitsgatheredevent_get_call.htm
tech.root: tapi
ms.assetid: 43625f93-4ab2-4aeb-83da-70310f118e34
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: ITDigitsGatheredEvent interface [TAPI 2.2],get_Call method, ITDigitsGatheredEvent.get_Call, ITDigitsGatheredEvent::get_Call, _tapi3_itdigitsgatheredevent_get_call, get_Call, get_Call method [TAPI 2.2], get_Call method [TAPI 2.2],ITDigitsGatheredEvent interface, tapi3.itdigitsgatheredevent_get_call, tapi3if/ITDigitsGatheredEvent::get_Call
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
 - ITDigitsGatheredEvent.get_Call
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITDigitsGatheredEvent::get_Call


## -description


The 
<b>get_Call</b> method gets a pointer to the call information interface for the call object on which the event occurred.


## -parameters




### -param ppCallInfo [out]

Pointer to the 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a> interface.


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
The <i>ppCallInfo</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/2d710bea-a0fd-492b-81a3-03b741685c91">ITDigitsGatheredEvent</a>
 

 

