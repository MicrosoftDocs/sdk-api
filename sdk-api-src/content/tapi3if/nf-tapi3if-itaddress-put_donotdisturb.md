---
UID: NF:tapi3if.ITAddress.put_DoNotDisturb
title: ITAddress::put_DoNotDisturb (tapi3if.h)
description: The put_DoNotDisturb method sets the do not disturb status. The do not disturb feature may not be available on all addresses.
helpviewer_keywords: ["ITAddress interface [TAPI 2.2]","put_DoNotDisturb method","ITAddress.put_DoNotDisturb","ITAddress::put_DoNotDisturb","_tapi3_itaddress_put_donotdisturb","put_DoNotDisturb","put_DoNotDisturb method [TAPI 2.2]","put_DoNotDisturb method [TAPI 2.2]","ITAddress interface","tapi3.itaddress_put_donotdisturb","tapi3if/ITAddress::put_DoNotDisturb"]
old-location: tapi3\itaddress_put_donotdisturb.htm
tech.root: tapi3
ms.assetid: 4d3071d5-055a-469d-aa17-984b8210cbea
ms.date: 12/05/2018
ms.keywords: ITAddress interface [TAPI 2.2],put_DoNotDisturb method, ITAddress.put_DoNotDisturb, ITAddress::put_DoNotDisturb, _tapi3_itaddress_put_donotdisturb, put_DoNotDisturb, put_DoNotDisturb method [TAPI 2.2], put_DoNotDisturb method [TAPI 2.2],ITAddress interface, tapi3.itaddress_put_donotdisturb, tapi3if/ITAddress::put_DoNotDisturb
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
 - ITAddress::put_DoNotDisturb
 - tapi3if/ITAddress::put_DoNotDisturb
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
 - ITAddress.put_DoNotDisturb
---

# ITAddress::put_DoNotDisturb


## -description

The 
<b>put_DoNotDisturb</b> method sets the do not disturb status. The do not disturb feature may not be available on all addresses.

## -parameters

### -param fDoNotDisturb [in]

If VARIANT_TRUE, the do not disturb feature will be activated. If VARIANT_FALSE, the do not disturb feature will be deactivated and all forwarding canceled.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>fDoNotDisturb</i> parameter is not a valid pointer.

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
<dt><b>TAPI_E_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The operation failed because the TAPI 3 DLL timed it out. The timeout interval is two minutes.

</td>
</tr>
</table>

## -remarks

The DoNotDisturb feature is implemented using forwarding. If 
<b>put_DoNotDisturb</b> is called with VARIANT_TRUE, Tapi3.dll creates a 
<a href="/windows/desktop/api/tapi/ns-tapi-lineforward">LINEFORWARD</a> list with the mode set to LINEFORWARDMODE_UNCOND and only one LINEFORWARD item with the destination address set to <b>NULL</b>. If 
<b>put_DoNotDisturb</b> is called with VARIANT_FALSE, Tapi3.dll cancels forwarding completely on this address, even those forwarding rules set with 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward">ITAddress::Forward</a>.

## -see-also

<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_donotdisturb">get_DoNotDisturb</a>