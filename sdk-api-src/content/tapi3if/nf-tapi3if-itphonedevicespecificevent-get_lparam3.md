---
UID: NF:tapi3if.ITPhoneDeviceSpecificEvent.get_lParam3
title: ITPhoneDeviceSpecificEvent::get_lParam3
author: windows-sdk-content
description: The get_lParam3 method retrieves the third of three buffers specific to a given phone device. The precise content and meaning of these buffers is defined by the provider.
old-location: tapi3\itphonedevicespecificevent_get_lparam3.htm
old-project: tapi
ms.assetid: 0dd4c5d7-033a-4e25-a7f0-6731b5b08d18
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: ITPhoneDeviceSpecificEvent interface [TAPI 2.2],get_lParam3 method, ITPhoneDeviceSpecificEvent.get_lParam3, ITPhoneDeviceSpecificEvent::get_lParam3, _tapi3_itphonedevicespecificevent_get_lparam3, get_lParam3, get_lParam3 method [TAPI 2.2], get_lParam3 method [TAPI 2.2],ITPhoneDeviceSpecificEvent interface, tapi3.itphonedevicespecificevent_get_lparam3, tapi3if/ITPhoneDeviceSpecificEvent::get_lParam3
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITPhoneDeviceSpecificEvent.get_lParam3
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
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




<a href="https://msdn.microsoft.com/a4b2fb49-6128-41b6-8eb3-13a8bbba66ac">ITPhoneDeviceSpecificEvent</a>



<a href="https://msdn.microsoft.com/236d4e7f-865f-4b26-8da6-c86476588c47">Phone and Address Device-specific Events</a>
 

 

