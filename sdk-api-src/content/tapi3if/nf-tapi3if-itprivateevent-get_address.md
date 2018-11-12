---
UID: NF:tapi3if.ITPrivateEvent.get_Address
title: ITPrivateEvent::get_Address
author: windows-sdk-content
description: The get_Address method gets the ITAddress interface pointer to the private object involved in the event.
old-location: tapi3\itprivateevent_get_address.htm
tech.root: tapi
ms.assetid: fa06ef5a-2aae-49e0-9fbb-473a5e2a0db3
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ITPrivateEvent interface [TAPI 2.2],get_Address method, ITPrivateEvent.get_Address, ITPrivateEvent::get_Address, _tapi3_itprivateevent_get_address, get_Address, get_Address method [TAPI 2.2], get_Address method [TAPI 2.2],ITPrivateEvent interface, tapi3.itprivateevent_get_address, tapi3if/ITPrivateEvent::get_Address
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
 - ITPrivateEvent.get_Address
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITPrivateEvent::get_Address


## -description


The 
<b>get_Address</b> method gets the 
<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a> interface pointer to the private object involved in the event.


## -parameters




### -param ppAddress [out]

Pointer to an 
<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a> interface.


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
The <i>ppAddress</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>



<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a>



<a href="https://msdn.microsoft.com/75a711e4-21b2-40a4-81f0-a210829178b9">ITPrivateEvent</a>
 

 

