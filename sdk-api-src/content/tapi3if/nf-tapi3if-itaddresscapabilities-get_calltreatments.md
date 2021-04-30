---
UID: NF:tapi3if.ITAddressCapabilities.get_CallTreatments
title: ITAddressCapabilities::get_CallTreatments (tapi3if.h)
description: The get_CallTreatments method gets call treatments. This method is provided for Automation client applications, such as those written in Visual Basic and scripting languages.
helpviewer_keywords: ["ITAddressCapabilities interface [TAPI 2.2]","get_CallTreatments method","ITAddressCapabilities.get_CallTreatments","ITAddressCapabilities::get_CallTreatments","_tapi3_itaddresscapabilities_get_calltreatments","get_CallTreatments","get_CallTreatments method [TAPI 2.2]","get_CallTreatments method [TAPI 2.2]","ITAddressCapabilities interface","tapi3.itaddresscapabilities_get_calltreatments","tapi3if/ITAddressCapabilities::get_CallTreatments"]
old-location: tapi3\itaddresscapabilities_get_calltreatments.htm
tech.root: tapi3
ms.assetid: fd6bbbf0-1f33-4e4f-bd81-7854019a0225
ms.date: 12/05/2018
ms.keywords: ITAddressCapabilities interface [TAPI 2.2],get_CallTreatments method, ITAddressCapabilities.get_CallTreatments, ITAddressCapabilities::get_CallTreatments, _tapi3_itaddresscapabilities_get_calltreatments, get_CallTreatments, get_CallTreatments method [TAPI 2.2], get_CallTreatments method [TAPI 2.2],ITAddressCapabilities interface, tapi3.itaddresscapabilities_get_calltreatments, tapi3if/ITAddressCapabilities::get_CallTreatments
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
 - ITAddressCapabilities::get_CallTreatments
 - tapi3if/ITAddressCapabilities::get_CallTreatments
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
 - ITAddressCapabilities.get_CallTreatments
---

# ITAddressCapabilities::get_CallTreatments


## -description

The 
<b>get_CallTreatments</b> method gets 
<a href="/windows/desktop/Tapi/linecalltreatment--constants">call treatments</a>. This method is provided for Automation client applications, such as those written in Visual Basic and scripting languages.

## -parameters

### -param pVariant [out]

Pointer to a <b>VARIANT</b> containing an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a> of call treatments.

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
<dt><b>TAPI_E_INVALCALLSTATE</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/tapi3if/ne-tapi3if-call_state">Call state</a> must be CS_IDLE.

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
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a> interface returned by <b>ITAddressCapabilities::get_CallTreatments</b>. The application must call <b>Release</b> on the 
<b>ITCallInfo</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities">ITAddressCapabilities</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a>