---
UID: NF:tapi3if.ITPhoneDeviceSpecificEvent.get_lParam2
title: ITPhoneDeviceSpecificEvent::get_lParam2
author: windows-sdk-content
description: The get_lParam2 method retrieves the second of three buffers specific to a given phone device. The precise content and meaning of these buffers is defined by the provider.
old-location: tapi3\itphonedevicespecificevent_get_lparam2.htm
tech.root: TAPI
ms.assetid: 58784ca2-ca2e-4a89-9b8c-3a6118b0ef2d
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ITPhoneDeviceSpecificEvent interface [TAPI 2.2],get_lParam2 method, ITPhoneDeviceSpecificEvent.get_lParam2, ITPhoneDeviceSpecificEvent::get_lParam2, _tapi3_itphonedevicespecificevent_get_lparam2, get_lParam2, get_lParam2 method [TAPI 2.2], get_lParam2 method [TAPI 2.2],ITPhoneDeviceSpecificEvent interface, tapi3.itphonedevicespecificevent_get_lparam2, tapi3if/ITPhoneDeviceSpecificEvent::get_lParam2
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
 - ITPhoneDeviceSpecificEvent.get_lParam2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITPhoneDeviceSpecificEvent::get_lParam2


## -description


The 
<b>get_lParam2</b> method retrieves the second of three buffers specific to a given phone device. The precise content and meaning of these buffers is defined by the provider.


## -parameters




### -param pParam2 [out]

Pointer to a <b>long</b> concerning information on the phone device event.


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




<a href="https://msdn.microsoft.com/a4b2fb49-6128-41b6-8eb3-13a8bbba66ac">ITPhoneDeviceSpecificEvent</a>



<a href="https://msdn.microsoft.com/236d4e7f-865f-4b26-8da6-c86476588c47">Phone and Address Device-specific Events</a>
 

 

