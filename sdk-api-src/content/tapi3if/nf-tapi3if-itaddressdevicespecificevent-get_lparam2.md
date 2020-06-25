---
UID: NF:tapi3if.ITAddressDeviceSpecificEvent.get_lParam2
title: ITAddressDeviceSpecificEvent::get_lParam2 (tapi3if.h)
description: The get_lParam2 method retrieves the second of three buffers specific to a given address device. The precise content and meaning of these buffers is defined by the provider.
helpviewer_keywords: ["ITAddressDeviceSpecificEvent interface [TAPI 2.2]","get_lParam2 method","ITAddressDeviceSpecificEvent.get_lParam2","ITAddressDeviceSpecificEvent::get_lParam2","_tapi3_itaddressdevicespecificevent_get_lparam2","get_lParam2","get_lParam2 method [TAPI 2.2]","get_lParam2 method [TAPI 2.2]","ITAddressDeviceSpecificEvent interface","tapi3.itaddressdevicespecificevent_get_lparam2","tapi3if/ITAddressDeviceSpecificEvent::get_lParam2"]
old-location: tapi3\itaddressdevicespecificevent_get_lparam2.htm
tech.root: Tapi
ms.assetid: b155cf6b-babd-4c47-8571-96f970878d81
ms.date: 12/05/2018
ms.keywords: ITAddressDeviceSpecificEvent interface [TAPI 2.2],get_lParam2 method, ITAddressDeviceSpecificEvent.get_lParam2, ITAddressDeviceSpecificEvent::get_lParam2, _tapi3_itaddressdevicespecificevent_get_lparam2, get_lParam2, get_lParam2 method [TAPI 2.2], get_lParam2 method [TAPI 2.2],ITAddressDeviceSpecificEvent interface, tapi3.itaddressdevicespecificevent_get_lparam2, tapi3if/ITAddressDeviceSpecificEvent::get_lParam2
f1_keywords:
- tapi3if/ITAddressDeviceSpecificEvent.get_lParam2
dev_langs:
- c++
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
- ITAddressDeviceSpecificEvent.get_lParam2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITAddressDeviceSpecificEvent::get_lParam2


## -description


The 
<b>get_lParam2</b> method retrieves the second of three buffers specific to a given address device. The precise content and meaning of these buffers is defined by the provider.


## -parameters




### -param pParam2 [out]

Pointer to a <b>long</b> concerning information on the address device event.


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
The <i>pParam2</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itaddressdevicespecificevent">ITAddressDeviceSpecificEvent</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/phone-and-address-device-specific-events">Phone and Address Device-specific Events</a>
 

 

