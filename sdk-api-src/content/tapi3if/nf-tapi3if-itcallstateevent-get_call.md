---
UID: NF:tapi3if.ITCallStateEvent.get_Call
title: ITCallStateEvent::get_Call
author: windows-sdk-content
description: The get_Call method gets a pointer to the call information interface for the call on which the event has occurred.
old-location: tapi3\itcallstateevent_get_call.htm
tech.root: tapi
ms.assetid: 942bd437-77d1-4d06-91d3-138b06f3228e
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITCallStateEvent interface [TAPI 2.2],get_Call method, ITCallStateEvent.get_Call, ITCallStateEvent::get_Call, _tapi3_itcallstateevent_get_call, get_Call, get_Call method [TAPI 2.2], get_Call method [TAPI 2.2],ITCallStateEvent interface, tapi3.itcallstateevent_get_call, tapi3if/ITCallStateEvent::get_Call
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
 - ITCallStateEvent.get_Call
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITCallStateEvent::get_Call


## -description


The 
<b>get_Call</b> method gets a pointer to the call information interface for the call on which the event has occurred.


## -parameters




### -param ppCallInfo [out]

Pointer to 
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
 




## -see-also




<a href="https://msdn.microsoft.com/67c063ba-8b12-40d6-9011-923bdee8b214">Call Object</a>



<a href="https://msdn.microsoft.com/0885ef81-726d-41ca-be8c-b3ff2e02fc3c">ITCallStateEvent</a>
 

 

