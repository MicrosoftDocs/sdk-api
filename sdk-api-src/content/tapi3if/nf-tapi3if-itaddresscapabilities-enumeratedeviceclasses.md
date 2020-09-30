---
UID: NF:tapi3if.ITAddressCapabilities.EnumerateDeviceClasses
title: ITAddressCapabilities::EnumerateDeviceClasses (tapi3if.h)
description: The EnumerateDeviceClasses method gets device classes. This method is provided for applications written in C/C++ and Java.
helpviewer_keywords: ["EnumerateDeviceClasses","EnumerateDeviceClasses method [TAPI 2.2]","EnumerateDeviceClasses method [TAPI 2.2]","ITAddressCapabilities interface","ITAddressCapabilities interface [TAPI 2.2]","EnumerateDeviceClasses method","ITAddressCapabilities.EnumerateDeviceClasses","ITAddressCapabilities::EnumerateDeviceClasses","_tapi3_itaddresscapabilities_enumeratedeviceclasses","tapi3.itaddresscapabilities_enumeratedeviceclasses","tapi3if/ITAddressCapabilities::EnumerateDeviceClasses"]
old-location: tapi3\itaddresscapabilities_enumeratedeviceclasses.htm
tech.root: tapi3
ms.assetid: 33cc965f-0603-40b0-95bb-9b16025dd2b6
ms.date: 12/05/2018
ms.keywords: EnumerateDeviceClasses, EnumerateDeviceClasses method [TAPI 2.2], EnumerateDeviceClasses method [TAPI 2.2],ITAddressCapabilities interface, ITAddressCapabilities interface [TAPI 2.2],EnumerateDeviceClasses method, ITAddressCapabilities.EnumerateDeviceClasses, ITAddressCapabilities::EnumerateDeviceClasses, _tapi3_itaddresscapabilities_enumeratedeviceclasses, tapi3.itaddresscapabilities_enumeratedeviceclasses, tapi3if/ITAddressCapabilities::EnumerateDeviceClasses
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
 - ITAddressCapabilities::EnumerateDeviceClasses
 - tapi3if/ITAddressCapabilities::EnumerateDeviceClasses
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
 - ITAddressCapabilities.EnumerateDeviceClasses
---

# ITAddressCapabilities::EnumerateDeviceClasses


## -description

The 
<b>EnumerateDeviceClasses</b> method gets device classes. This method is provided for applications written in C/C++ and Java.

## -parameters

### -param ppEnumDeviceClass [out]

Pointer to enumeration of 
<a href="/windows/desktop/Tapi/tapi-device-classes">device classes</a>.

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

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumbstr">IEnumBstr</a> interface returned by <b>ITAddressCapabilities::EnumerateDeviceClasses</b>. The application must call <b>Release</b> on the 
<b>IEnumBstr</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumbstr">IEnumBstr</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities">ITAddressCapabilities</a>