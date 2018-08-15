---
UID: NF:tapi3if.ITPhone.DeviceSpecific
title: ITPhone::DeviceSpecific
author: windows-sdk-content
description: The DeviceSpecific method enables service providers to provide access to device specific features not offered by other TAPI functions.
old-location: tapi3\itphone_devicespecific.htm
old-project: tapi
ms.assetid: fba4bf7e-8c9d-4d34-ac56-aa47dff6f57c
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: DeviceSpecific, DeviceSpecific method [TAPI 2.2], DeviceSpecific method [TAPI 2.2],ITPhone interface, ITPhone interface [TAPI 2.2],DeviceSpecific method, ITPhone.DeviceSpecific, ITPhone::DeviceSpecific, _tapi3_itphone_devicespecific, tapi3.itphone_devicespecific, tapi3if/ITPhone::DeviceSpecific
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
 - ITPhone.DeviceSpecific
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITPhone::DeviceSpecific


## -description


The 
<b>DeviceSpecific</b> method enables service providers to provide access to device specific features not offered by other TAPI functions. The meaning of the extensions are device specific, and taking advantage of these extensions requires the application to be fully aware of them.

This method is provided for C and C++ applications. Automation client applications, such as those written in Visual Basic, must use the 
<a href="https://msdn.microsoft.com/27882bb2-dab8-4b8c-acca-35fbdc526362">DeviceSpecificVariant</a> method.


## -parameters




### -param pParams [in]

Pointer to a memory area used to hold a parameter block. The format of this parameter block is device specific; TAPI passes its contents between the application and the service provider.


### -param dwSize [in]

The size, in bytes, of the parameter block area.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pParams</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/27882bb2-dab8-4b8c-acca-35fbdc526362">DeviceSpecificVariant</a>



<a href="https://msdn.microsoft.com/219b5c74-f999-4bb7-9e13-59c6ade9da46">NegotiateExtVersion</a>



<a href="https://msdn.microsoft.com/28f43b21-5118-465f-95b3-036aab16a049">lineDevSpecific</a>
 

 

