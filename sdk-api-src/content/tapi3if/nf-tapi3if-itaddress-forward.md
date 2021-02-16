---
UID: NF:tapi3if.ITAddress.Forward
title: ITAddress::Forward (tapi3if.h)
description: The Forward method forwards calls destined for the address according to the forwarding instructions contained in ITForwardInformation. If pForwardInfo is set to NULL, forwarding is canceled.
helpviewer_keywords: ["Forward","Forward method [TAPI 2.2]","Forward method [TAPI 2.2]","ITAddress interface","ITAddress interface [TAPI 2.2]","Forward method","ITAddress.Forward","ITAddress::Forward","_tapi3_itaddress_forward","tapi3.itaddress_forward","tapi3if/ITAddress::Forward"]
old-location: tapi3\itaddress_forward.htm
tech.root: tapi3
ms.assetid: 4f070b50-db9a-49e8-a0f3-e448c5dee144
ms.date: 12/05/2018
ms.keywords: Forward, Forward method [TAPI 2.2], Forward method [TAPI 2.2],ITAddress interface, ITAddress interface [TAPI 2.2],Forward method, ITAddress.Forward, ITAddress::Forward, _tapi3_itaddress_forward, tapi3.itaddress_forward, tapi3if/ITAddress::Forward
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
 - ITAddress::Forward
 - tapi3if/ITAddress::Forward
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
 - ITAddress.Forward
---

# ITAddress::Forward


## -description

The 
Forward method forwards calls destined for the address according to the forwarding instructions contained in 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation">ITForwardInformation</a>. If <i>pForwardInfo</i> is set to <b>NULL</b>, forwarding is canceled.

## -parameters

### -param pForwardInfo [in]

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation">ITForwardInformation</a> interface, or set to <b>NULL</b> to cancel forwarding.

### -param pCall [in]

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol">ITBasicCallControl</a> interface for the consultation call, if required by the telephony environment. May be <b>NULL</b> if not required.

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
The address does not support forwarding, or <i>pCall</i> does not point to a valid call.

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
The <i>pForwardInfo</i> or <i>pCall</i> parameter is not a valid pointer.

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
<tr>
<td width="40%">
<dl>
<dt><b>LINEERR_</b></dt>
</dl>
</td>
<td width="60%">
See 
<a href="/windows/desktop/api/tapi/nf-tapi-lineforward">LineForward</a> for error codes returned from this TAPI 2.1 function.

</td>
</tr>
</table>

## -remarks

The information in <i>pForwardInfo</i> overrides any previous forwarding instructions.

If 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-put_donotdisturb">ITAddress::put_DoNotDisturb</a> is called with <i>fDoNotDisturb</i> set to VARIANT_FALSE, all forwarding is canceled.

An application can determine whether non-<b>NULL</b> consultation call is required by calling 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability">ITAddressCapabilities::get_AddressCapability</a> (AC_ADDRESSCAPFLAGS, <i>plCapability</i>) and checking whether the flag LINEADDRCAPFLAGS_FWDCONSULT, a member of 
<a href="/windows/desktop/Tapi/lineaddrcapflags--constants">LINEADDRCAPFLAGS_ Constants</a>, has been set in <i>plCapability</i>. If it is set, a non-<b>NULL</b> value is required for the <i>pCall</i> parameter of the 
Forward method.

The 
Forward method is, in part, a COM wrapper for the TAPI 2.1 
<a href="/windows/desktop/api/tapi/nf-tapi-lineforward">LineForward</a> function.

## -see-also

<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/windows/desktop/Tapi/forward-ovr">Forward overview</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createforwardinfoobject">ITAddress::CreateForwardInfoObject</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_currentforwardinfo">ITAddress::get_CurrentForwardInfo</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation">ITForwardInformation</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineforward">LineForward</a>