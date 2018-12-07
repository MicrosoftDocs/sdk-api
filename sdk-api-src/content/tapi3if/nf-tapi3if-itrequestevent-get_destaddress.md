---
UID: NF:tapi3if.ITRequestEvent.get_DestAddress
title: ITRequestEvent::get_DestAddress
author: windows-sdk-content
description: The get_DestAddress method gets the destination address.
old-location: tapi3\itrequestevent_get_destaddress.htm
tech.root: tapi
ms.assetid: b3cf5a48-6d9f-4c66-91eb-c18a29d71ff9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITRequestEvent interface [TAPI 2.2],get_DestAddress method, ITRequestEvent.get_DestAddress, ITRequestEvent::get_DestAddress, _tapi3_itrequestevent_get_destaddress, get_DestAddress, get_DestAddress method [TAPI 2.2], get_DestAddress method [TAPI 2.2],ITRequestEvent interface, tapi3.itrequestevent_get_destaddress, tapi3if/ITRequestEvent::get_DestAddress
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
 - ITRequestEvent.get_DestAddress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITRequestEvent::get_DestAddress


## -description


The 
<b>get_DestAddress</b> method gets the destination address.


## -parameters




### -param ppDestAddress [out]

Pointer to a <b>BSTR</b> containing the destination address.


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
The <i>ppDestAddress</i> is not a valid pointer.

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



The application must use 
<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> to free the memory allocated for the <i>ppDestAddress</i> parameter.
			




## -see-also




<a href="https://msdn.microsoft.com/69f9b504-be01-4167-8002-32a8e86bab0f">ITRequestEvent</a>
 

 

