---
UID: NF:tapi3if.ITPhone.DeviceSpecificVariant
title: ITPhone::DeviceSpecificVariant
author: windows-sdk-content
description: The DeviceSpecificVariant method enables service providers to provide access to features not offered by other TAPI functions.
old-location: tapi3\itphone_devicespecificvariant.htm
old-project: tapi
ms.assetid: 828d34e5-efac-4776-85a2-51eb94d68dac
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: DeviceSpecificVariant, DeviceSpecificVariant method [TAPI 2.2], DeviceSpecificVariant method [TAPI 2.2],ITPhone interface, ITPhone interface [TAPI 2.2],DeviceSpecificVariant method, ITPhone.DeviceSpecificVariant, ITPhone::DeviceSpecificVariant, _tapi3_itphone_devicespecificvariant, tapi3.itphone_devicespecificvariant, tapi3if/ITPhone::DeviceSpecificVariant
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
req.redist: 
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
 - ITPhone.DeviceSpecificVariant
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITPhone::DeviceSpecificVariant


## -description


The 
<b>DeviceSpecificVariant</b> method enables service providers to provide access to features not offered by other TAPI functions. The meaning of the extensions are device specific, and taking advantage of these extensions requires the application to be fully aware of them.

This method is provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the 
<a href="https://msdn.microsoft.com/fba4bf7e-8c9d-4d34-ac56-aa47dff6f57c">DeviceSpecific</a> method.


## -parameters




### -param varDevSpecificByteArray [in]

VARIANT containing the parameter block. The format of this parameter block is device specific; TAPI passes its contents between the application and the service provider.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d3b9e04d-ec20-4e30-847f-eb77f426f0f3">DeviceSpecific</a>



<a href="https://msdn.microsoft.com/219b5c74-f999-4bb7-9e13-59c6ade9da46">NegotiateExtVersion</a>



<a href="https://msdn.microsoft.com/28f43b21-5118-465f-95b3-036aab16a049">lineDevSpecific</a>
 

 

