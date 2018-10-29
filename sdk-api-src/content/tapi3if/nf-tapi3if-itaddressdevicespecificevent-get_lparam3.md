---
UID: NF:tapi3if.ITAddressDeviceSpecificEvent.get_lParam3
title: ITAddressDeviceSpecificEvent::get_lParam3
author: windows-sdk-content
description: The get_lParam3 method retrieves the third of three buffers specific to a given address device. The precise content and meaning of these buffers is defined by the provider.
old-location: tapi3\itaddressdevicespecificevent_get_lparam3.htm
tech.root: Tapi
ms.assetid: 8e0a513d-2bf4-4bdf-926f-2e88a8465073
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ITAddressDeviceSpecificEvent interface [TAPI 2.2],get_lParam3 method, ITAddressDeviceSpecificEvent.get_lParam3, ITAddressDeviceSpecificEvent::get_lParam3, _tapi3_itaddressdevicespecificevent_get_lparam3, get_lParam3, get_lParam3 method [TAPI 2.2], get_lParam3 method [TAPI 2.2],ITAddressDeviceSpecificEvent interface, tapi3.itaddressdevicespecificevent_get_lparam3, tapi3if/ITAddressDeviceSpecificEvent::get_lParam3
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
 - ITAddressDeviceSpecificEvent.get_lParam3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAddressDeviceSpecificEvent::get_lParam3


## -description


The 
<b>get_lParam3</b> method retrieves the third of three buffers specific to a given address device. The precise content and meaning of these buffers is defined by the provider.


## -parameters




### -param pParam3 [out]

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
The <i>pParam3</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/8590e9b1-2bbf-47e5-96de-8765a475a972">ITAddressDeviceSpecificEvent</a>



<a href="https://msdn.microsoft.com/236d4e7f-865f-4b26-8da6-c86476588c47">Phone and Address Device-specific Events</a>
 

 

