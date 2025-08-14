---
UID: NF:tapi3if.ITPhone.DeviceSpecific
title: ITPhone::DeviceSpecific (tapi3if.h)
description: The DeviceSpecific method enables service providers to provide access to device specific features not offered by other TAPI functions.
helpviewer_keywords: ["DeviceSpecific","DeviceSpecific method [TAPI 2.2]","DeviceSpecific method [TAPI 2.2]","ITPhone interface","ITPhone interface [TAPI 2.2]","DeviceSpecific method","ITPhone.DeviceSpecific","ITPhone::DeviceSpecific","_tapi3_itphone_devicespecific","tapi3.itphone_devicespecific","tapi3if/ITPhone::DeviceSpecific"]
old-location: tapi3\itphone_devicespecific.htm
tech.root: tapi3
ms.assetid: fba4bf7e-8c9d-4d34-ac56-aa47dff6f57c
ms.date: 12/05/2018
ms.keywords: DeviceSpecific, DeviceSpecific method [TAPI 2.2], DeviceSpecific method [TAPI 2.2],ITPhone interface, ITPhone interface [TAPI 2.2],DeviceSpecific method, ITPhone.DeviceSpecific, ITPhone::DeviceSpecific, _tapi3_itphone_devicespecific, tapi3.itphone_devicespecific, tapi3if/ITPhone::DeviceSpecific
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITPhone::DeviceSpecific
 - tapi3if/ITPhone::DeviceSpecific
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITPhone.DeviceSpecific
---

# ITPhone::DeviceSpecific


## -description

The 
<b>DeviceSpecific</b> method enables service providers to provide access to device specific features not offered by other TAPI functions. The meaning of the extensions are device specific, and taking advantage of these extensions requires the application to be fully aware of them.

This method is provided for C and C++ applications. Automation client applications, such as those written in Visual Basic, must use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress2-devicespecificvariant">DeviceSpecificVariant</a> method.

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

## -remarks

> [!CAUTION]
> TAPI will write the returned data to the buffer referenced by *pParams* when the [LINE_REPLY](/windows/win32/tapi/line-reply) message is returned. This means that the buffer must remain valid until the LINE_REPLY message is returned; otherwise, data corruption and exceptions may occur.


## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress2-devicespecificvariant">DeviceSpecificVariant</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress2-negotiateextversion">NegotiateExtVersion</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linedevspecific">lineDevSpecific</a>