---
UID: NF:tapi3if.ITPhone.DeviceSpecificVariant
title: ITPhone::DeviceSpecificVariant (tapi3if.h)
description: The DeviceSpecificVariant method enables service providers to provide access to features not offered by other TAPI functions. (ITPhone.DeviceSpecificVariant)
helpviewer_keywords: ["DeviceSpecificVariant","DeviceSpecificVariant method [TAPI 2.2]","DeviceSpecificVariant method [TAPI 2.2]","ITPhone interface","ITPhone interface [TAPI 2.2]","DeviceSpecificVariant method","ITPhone.DeviceSpecificVariant","ITPhone::DeviceSpecificVariant","_tapi3_itphone_devicespecificvariant","tapi3.itphone_devicespecificvariant","tapi3if/ITPhone::DeviceSpecificVariant"]
old-location: tapi3\itphone_devicespecificvariant.htm
tech.root: tapi3
ms.assetid: 828d34e5-efac-4776-85a2-51eb94d68dac
ms.date: 12/05/2018
ms.keywords: DeviceSpecificVariant, DeviceSpecificVariant method [TAPI 2.2], DeviceSpecificVariant method [TAPI 2.2],ITPhone interface, ITPhone interface [TAPI 2.2],DeviceSpecificVariant method, ITPhone.DeviceSpecificVariant, ITPhone::DeviceSpecificVariant, _tapi3_itphone_devicespecificvariant, tapi3.itphone_devicespecificvariant, tapi3if/ITPhone::DeviceSpecificVariant
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
 - ITPhone::DeviceSpecificVariant
 - tapi3if/ITPhone::DeviceSpecificVariant
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
 - ITPhone.DeviceSpecificVariant
---

# ITPhone::DeviceSpecificVariant


## -description

The 
<b>DeviceSpecificVariant</b> method enables service providers to provide access to features not offered by other TAPI functions. The meaning of the extensions are device specific, and taking advantage of these extensions requires the application to be fully aware of them.

This method is provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-devicespecific">DeviceSpecific</a> method.

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

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress2-devicespecific">DeviceSpecific</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress2-negotiateextversion">NegotiateExtVersion</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linedevspecific">lineDevSpecific</a>
