---
UID: NF:tapi3if.ITAddressCapabilities.get_DeviceClasses
title: ITAddressCapabilities::get_DeviceClasses
author: windows-sdk-content
description: The get_DeviceClasses method gets device classes. This method is provided for Automation client applications, such as those written in Visual Basic and scripting languages.
old-location: tapi3\itaddresscapabilities_get_deviceclasses.htm
tech.root: tapi
ms.assetid: 34c662c6-4166-470f-aaaf-001da4ed048a
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITAddressCapabilities interface [TAPI 2.2],get_DeviceClasses method, ITAddressCapabilities.get_DeviceClasses, ITAddressCapabilities::get_DeviceClasses, _tapi3_itaddresscapabilities_get_deviceclasses, get_DeviceClasses, get_DeviceClasses method [TAPI 2.2], get_DeviceClasses method [TAPI 2.2],ITAddressCapabilities interface, tapi3.itaddresscapabilities_get_deviceclasses, tapi3if/ITAddressCapabilities::get_DeviceClasses
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
 - ITAddressCapabilities.get_DeviceClasses
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAddressCapabilities::get_DeviceClasses


## -description


The 
<b>get_DeviceClasses</b> method gets device classes. This method is provided for Automation client applications, such as those written in Visual Basic and scripting languages.


## -parameters




### -param pVariant [out]

Pointer to <b>VARIANT</b> containing 
<a href="https://msdn.microsoft.com/859979a8-0d16-4b7b-b183-d6e30f3e034d">device classes</a>.


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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Method not implemented.

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




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>



<a href="https://msdn.microsoft.com/36f452ce-9171-41da-b003-4c7df17790da">ITAddressCapabilities</a>
 

 

