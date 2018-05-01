---
UID: NF:tapi3if.ITPhoneDeviceSpecificEvent.get_Phone
title: ITPhoneDeviceSpecificEvent::get_Phone method
author: windows-driver-content
description: The get_Phone method retrieves the ITPhone interface pointer for a phone device event.
old-location: tapi3\itphonedevicespecificevent_get_phone.htm
old-project: Tapi
ms.assetid: 068f4172-92a4-41cc-b554-c6e4014505eb
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: ITPhoneDeviceSpecificEvent, ITPhoneDeviceSpecificEvent interface [TAPI 2.2], get_Phone method, ITPhoneDeviceSpecificEvent::get_Phone, _tapi3_itphonedevicespecificevent_get_phone, get_Phone method [TAPI 2.2], get_Phone method [TAPI 2.2], ITPhoneDeviceSpecificEvent interface, get_Phone,ITPhoneDeviceSpecificEvent.get_Phone, tapi3.itphonedevicespecificevent_get_phone, tapi3if/ITPhoneDeviceSpecificEvent::get_Phone
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
req.typenames: TERMINAL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	ITPhoneDeviceSpecificEvent.get_Phone
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITPhoneDeviceSpecificEvent::get_Phone method


## -description


The 
<b>get_Phone</b> method retrieves the 
<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a> interface pointer for a phone device event.


## -parameters




### -param ppPhone [out]

Pointer to the 
<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a> interface for the phone object involved in the event.


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
The <i>ppPhone</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a>



<a href="https://msdn.microsoft.com/a4b2fb49-6128-41b6-8eb3-13a8bbba66ac">ITPhoneDeviceSpecificEvent</a>
 

 

