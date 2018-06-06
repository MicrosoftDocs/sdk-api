---
UID: NF:tapi3if.ITAddress2.DeviceSpecificVariant
title: ITAddress2::DeviceSpecificVariant
author: windows-sdk-content
description: The DeviceSpecificVariant method enables service providers to provide access to features not offered by other TAPI functions.
old-location: tapi3\itaddress2_devicespecificvariant.htm
old-project: Tapi
ms.assetid: 27882bb2-dab8-4b8c-acca-35fbdc526362
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: DeviceSpecificVariant, DeviceSpecificVariant method [TAPI 2.2], DeviceSpecificVariant method [TAPI 2.2],ITAddress2 interface, ITAddress2 interface [TAPI 2.2],DeviceSpecificVariant method, ITAddress2.DeviceSpecificVariant, ITAddress2::DeviceSpecificVariant, _tapi3_itaddress2_devicespecificvariant, tapi3.itaddress2_devicespecificvariant, tapi3if/ITAddress2::DeviceSpecificVariant
ms.prod: windows
ms.technology: windows-sdk
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
 - ITAddress2.DeviceSpecificVariant
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAddress2::DeviceSpecificVariant


## -description


The 
<b>DeviceSpecificVariant</b> method enables service providers to provide access to features not offered by other TAPI functions. The meaning of the extensions are device specific, and taking advantage of these extensions requires the application to be fully aware of them.

This method is provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the 
<a href="https://msdn.microsoft.com/d3b9e04d-ec20-4e30-847f-eb77f426f0f3">DeviceSpecific</a> method.


## -parameters




### -param pCall [in]

Pointer to the 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a> interface of the call object.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pCall</i> parameter is not a valid pointer.

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
 

 

