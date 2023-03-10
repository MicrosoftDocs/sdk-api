---
UID: NF:tapi3if.ITAddress.get_DoNotDisturb
title: ITAddress::get_DoNotDisturb (tapi3if.h)
description: The get_DoNotDisturb method gets the current status of the do not disturb feature on the address. The do not disturb feature may not be available on all addresses.
helpviewer_keywords: ["ITAddress interface [TAPI 2.2]","get_DoNotDisturb method","ITAddress.get_DoNotDisturb","ITAddress::get_DoNotDisturb","_tapi3_itaddress_get_donotdisturb","get_DoNotDisturb","get_DoNotDisturb method [TAPI 2.2]","get_DoNotDisturb method [TAPI 2.2]","ITAddress interface","tapi3.itaddress_get_donotdisturb","tapi3if/ITAddress::get_DoNotDisturb"]
old-location: tapi3\itaddress_get_donotdisturb.htm
tech.root: tapi3
ms.assetid: d9257201-bcd1-4d6b-9bc7-24b323cd4f15
ms.date: 12/05/2018
ms.keywords: ITAddress interface [TAPI 2.2],get_DoNotDisturb method, ITAddress.get_DoNotDisturb, ITAddress::get_DoNotDisturb, _tapi3_itaddress_get_donotdisturb, get_DoNotDisturb, get_DoNotDisturb method [TAPI 2.2], get_DoNotDisturb method [TAPI 2.2],ITAddress interface, tapi3.itaddress_get_donotdisturb, tapi3if/ITAddress::get_DoNotDisturb
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
 - ITAddress::get_DoNotDisturb
 - tapi3if/ITAddress::get_DoNotDisturb
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
 - ITAddress.get_DoNotDisturb
---

# ITAddress::get_DoNotDisturb


## -description

The 
<b>get_DoNotDisturb</b> method gets the current status of the do not disturb feature on the address. The do not disturb feature may not be available on all addresses.

## -parameters

### -param pfDoNotDisturb [out]

If VARIANT_TRUE, the do not disturb feature has been activated. If VARIANT_FALSE, the do not disturb feature is not active.

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
<dt><b>E_OPERATIONUNAVAIL</b></dt>
</dl>
</td>
<td width="60%">
Operation unavailable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_NOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
This operation is not supported on this address.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pfDoNotDisturb</i> parameter is not a valid pointer.

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

For programmers familiar with TAPI 2.<i>x:</i> The DoNotDisturb feature is implemented using the "forward" feature, if present on the address. When 
<b>get_DoNotDisturb</b> is called, Tapi3.dll gets the 
<a href="/windows/desktop/api/tapi/ns-tapi-lineaddressstatus">LINEADDRESSSTATUS</a> of the address object, and looks for its 
<a href="/windows/desktop/api/tapi/ns-tapi-lineforward">LINEFORWARD</a> entries. If one such entry is found and if its <i>dwDestAddressOffset</i> member is 0 (zero), then DoNotDisturb is considered to be turned ON, and therefore VARIANT_TRUE is returned as the value for this method.

## -see-also

<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-put_donotdisturb">put_DoNotDisturb</a>