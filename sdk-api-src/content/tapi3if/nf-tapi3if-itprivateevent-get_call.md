---
UID: NF:tapi3if.ITPrivateEvent.get_Call
title: ITPrivateEvent::get_Call
author: windows-sdk-content
description: The get_Call method returns a pointer to the ITCallInfo interface of the call on which the event occurred.
old-location: tapi3\itprivateevent_get_call.htm
tech.root: tapi
ms.assetid: 3d4db0b3-9bff-4e14-9fe2-549934c2d244
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ITPrivateEvent interface [TAPI 2.2],get_Call method, ITPrivateEvent.get_Call, ITPrivateEvent::get_Call, _tapi3_itprivateevent_get_call, get_Call, get_Call method [TAPI 2.2], get_Call method [TAPI 2.2],ITPrivateEvent interface, tapi3.itprivateevent_get_call, tapi3if/ITPrivateEvent::get_Call
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tapi3if.h
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
 - ITPrivateEvent.get_Call
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITPrivateEvent::get_Call


## -description


The 
<b>get_Call</b> method returns a pointer to the 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a> interface of the call on which the event occurred.


## -parameters




### -param ppCallInfo [out]

 Pointer to the 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a> interface.


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
The <i>ppCallInfo</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a>



<a href="https://msdn.microsoft.com/75a711e4-21b2-40a4-81f0-a210829178b9">ITPrivateEvent</a>
 

 

