---
UID: NF:tapi3if.ITAddress.get_Calls
title: ITAddress::get_Calls (tapi3if.h)
description: The get_Calls method creates a collection of calls currently active on the address. This method is provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the EnumerateCalls method.
helpviewer_keywords: ["ITAddress interface [TAPI 2.2]","get_Calls method","ITAddress.get_Calls","ITAddress::get_Calls","_tapi3_itaddress_get_calls","get_Calls","get_Calls method [TAPI 2.2]","get_Calls method [TAPI 2.2]","ITAddress interface","tapi3.itaddress_get_calls","tapi3if/ITAddress::get_Calls"]
old-location: tapi3\itaddress_get_calls.htm
tech.root: tapi3
ms.assetid: b0b16578-0530-4ff9-a7ce-d36527ed2da9
ms.date: 12/05/2018
ms.keywords: ITAddress interface [TAPI 2.2],get_Calls method, ITAddress.get_Calls, ITAddress::get_Calls, _tapi3_itaddress_get_calls, get_Calls, get_Calls method [TAPI 2.2], get_Calls method [TAPI 2.2],ITAddress interface, tapi3.itaddress_get_calls, tapi3if/ITAddress::get_Calls
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
 - ITAddress::get_Calls
 - tapi3if/ITAddress::get_Calls
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
 - ITAddress.get_Calls
---

# ITAddress::get_Calls


## -description

The 
<b>get_Calls</b> method creates a collection of calls currently active on the address. This method is provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-enumeratecalls">EnumerateCalls</a> method.

## -parameters

### -param pVariant [out]

Pointer to a <b>VARIANT</b> containing an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a> of 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a> interface pointers (call objects).

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
The <i>pVariant</i> parameter is not a valid pointer.

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
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a> interface returned by ITAddress::get_Calls. The application must call <b>Release</b> on the 
<b>ITCallInfo</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-enumeratecalls">EnumerateCalls</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a>