---
UID: NF:tapi3if.ITPhoneDeviceSpecificEvent.get_lParam3
title: ITPhoneDeviceSpecificEvent::get_lParam3 (tapi3if.h)
description: The get_lParam3 method retrieves the third of three buffers specific to a given phone device. The precise content and meaning of these buffers is defined by the provider.
helpviewer_keywords: ["ITPhoneDeviceSpecificEvent interface [TAPI 2.2]","get_lParam3 method","ITPhoneDeviceSpecificEvent.get_lParam3","ITPhoneDeviceSpecificEvent::get_lParam3","_tapi3_itphonedevicespecificevent_get_lparam3","get_lParam3","get_lParam3 method [TAPI 2.2]","get_lParam3 method [TAPI 2.2]","ITPhoneDeviceSpecificEvent interface","tapi3.itphonedevicespecificevent_get_lparam3","tapi3if/ITPhoneDeviceSpecificEvent::get_lParam3"]
old-location: tapi3\itphonedevicespecificevent_get_lparam3.htm
tech.root: tapi3
ms.assetid: 0dd4c5d7-033a-4e25-a7f0-6731b5b08d18
ms.date: 12/05/2018
ms.keywords: ITPhoneDeviceSpecificEvent interface [TAPI 2.2],get_lParam3 method, ITPhoneDeviceSpecificEvent.get_lParam3, ITPhoneDeviceSpecificEvent::get_lParam3, _tapi3_itphonedevicespecificevent_get_lparam3, get_lParam3, get_lParam3 method [TAPI 2.2], get_lParam3 method [TAPI 2.2],ITPhoneDeviceSpecificEvent interface, tapi3.itphonedevicespecificevent_get_lparam3, tapi3if/ITPhoneDeviceSpecificEvent::get_lParam3
f1_keywords:
- tapi3if/ITPhoneDeviceSpecificEvent.get_lParam3
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
- ITPhoneDeviceSpecificEvent.get_lParam3
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITPhoneDeviceSpecificEvent::get_lParam3


## -description


The 
<b>get_lParam3</b> method retrieves the third of three buffers specific to a given phone device. The precise content and meaning of these buffers is defined by the provider.


## -parameters




### -param pParam3 [out]

Pointer to a variable that receives information on the phone device event.


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
The <i>pParam3</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itphonedevicespecificevent">ITPhoneDeviceSpecificEvent</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/phone-and-address-device-specific-events">Phone and Address Device-specific Events</a>
 

 

