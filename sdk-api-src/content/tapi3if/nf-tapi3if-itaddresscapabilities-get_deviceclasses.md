---
UID: NF:tapi3if.ITAddressCapabilities.get_DeviceClasses
title: ITAddressCapabilities::get_DeviceClasses (tapi3if.h)
description: The get_DeviceClasses method gets device classes. This method is provided for Automation client applications, such as those written in Visual Basic and scripting languages.
helpviewer_keywords: ["ITAddressCapabilities interface [TAPI 2.2]","get_DeviceClasses method","ITAddressCapabilities.get_DeviceClasses","ITAddressCapabilities::get_DeviceClasses","_tapi3_itaddresscapabilities_get_deviceclasses","get_DeviceClasses","get_DeviceClasses method [TAPI 2.2]","get_DeviceClasses method [TAPI 2.2]","ITAddressCapabilities interface","tapi3.itaddresscapabilities_get_deviceclasses","tapi3if/ITAddressCapabilities::get_DeviceClasses"]
old-location: tapi3\itaddresscapabilities_get_deviceclasses.htm
tech.root: tapi3
ms.assetid: 34c662c6-4166-470f-aaaf-001da4ed048a
ms.date: 12/05/2018
ms.keywords: ITAddressCapabilities interface [TAPI 2.2],get_DeviceClasses method, ITAddressCapabilities.get_DeviceClasses, ITAddressCapabilities::get_DeviceClasses, _tapi3_itaddresscapabilities_get_deviceclasses, get_DeviceClasses, get_DeviceClasses method [TAPI 2.2], get_DeviceClasses method [TAPI 2.2],ITAddressCapabilities interface, tapi3.itaddresscapabilities_get_deviceclasses, tapi3if/ITAddressCapabilities::get_DeviceClasses
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
 - ITAddressCapabilities::get_DeviceClasses
 - tapi3if/ITAddressCapabilities::get_DeviceClasses
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
 - ITAddressCapabilities.get_DeviceClasses
---

# ITAddressCapabilities::get_DeviceClasses


## -description

The 
<b>get_DeviceClasses</b> method gets device classes. This method is provided for Automation client applications, such as those written in Visual Basic and scripting languages.

## -parameters

### -param pVariant [out]

Pointer to <b>VARIANT</b> containing 
<a href="/windows/desktop/Tapi/tapi-device-classes">device classes</a>.

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

<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities">ITAddressCapabilities</a>