---
UID: NF:tapi3if.ITAddress2.DeviceSpecific
title: ITAddress2::DeviceSpecific (tapi3if.h)
author: windows-sdk-content
description: The DeviceSpecific method enables service providers to provide access to features not offered by other TAPI functions.
old-location: tapi3\itaddress2_devicespecific.htm
tech.root: Tapi
ms.assetid: d3b9e04d-ec20-4e30-847f-eb77f426f0f3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DeviceSpecific, DeviceSpecific method [TAPI 2.2], DeviceSpecific method [TAPI 2.2],ITAddress2 interface, ITAddress2 interface [TAPI 2.2],DeviceSpecific method, ITAddress2.DeviceSpecific, ITAddress2::DeviceSpecific, _tapi3_itaddress2_devicespecific, tapi3.itaddress2_devicespecific, tapi3if/ITAddress2::DeviceSpecific
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
 - ITAddress2.DeviceSpecific
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAddress2::DeviceSpecific


## -description


The 
<b>DeviceSpecific</b> method enables service providers to provide access to features not offered by other TAPI functions. The meaning of the extensions are device specific, and taking advantage of these extensions requires the application to be fully aware of them.

This method is provided for C and C++ applications. Automation client applications, such as those written in Visual Basic, must use the 
<a href="https://msdn.microsoft.com/27882bb2-dab8-4b8c-acca-35fbdc526362">DeviceSpecificVariant</a> method.


## -parameters




### -param pCall [in]

Pointer to the 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a> interface of the call object.


### -param pParams [in]

Pointer to a memory area used to hold a parameter block. The format of this parameter block is device specific; TAPI passes its contents between the application and the service provider.


### -param dwSize [in]

Size, in bytes, of the parameter block area.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pParams</i> or <i>pCall</i> parameter is not a valid pointer.

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




<a href="https://msdn.microsoft.com/27882bb2-dab8-4b8c-acca-35fbdc526362">DeviceSpecificVariant</a>



<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a>



<a href="https://msdn.microsoft.com/219b5c74-f999-4bb7-9e13-59c6ade9da46">NegotiateExtVersion</a>



<a href="https://msdn.microsoft.com/28f43b21-5118-465f-95b3-036aab16a049">lineDevSpecific</a>
 

 

