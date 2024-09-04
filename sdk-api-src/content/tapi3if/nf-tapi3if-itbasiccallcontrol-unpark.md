---
UID: NF:tapi3if.ITBasicCallControl.Unpark
title: ITBasicCallControl::Unpark (tapi3if.h)
description: The Unpark method gets the call from park.
helpviewer_keywords: ["ITBasicCallControl interface [TAPI 2.2]","Unpark method","ITBasicCallControl.Unpark","ITBasicCallControl::Unpark","Unpark","Unpark method [TAPI 2.2]","Unpark method [TAPI 2.2]","ITBasicCallControl interface","_tapi3_itbasiccallcontrol_unpark","tapi3.itbasiccallcontrol_unpark","tapi3if/ITBasicCallControl::Unpark"]
old-location: tapi3\itbasiccallcontrol_unpark.htm
tech.root: tapi3
ms.assetid: d4cea44e-0dac-4021-a42c-b136c2e686e0
ms.date: 12/05/2018
ms.keywords: ITBasicCallControl interface [TAPI 2.2],Unpark method, ITBasicCallControl.Unpark, ITBasicCallControl::Unpark, Unpark, Unpark method [TAPI 2.2], Unpark method [TAPI 2.2],ITBasicCallControl interface, _tapi3_itbasiccallcontrol_unpark, tapi3.itbasiccallcontrol_unpark, tapi3if/ITBasicCallControl::Unpark
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
 - ITBasicCallControl::Unpark
 - tapi3if/ITBasicCallControl::Unpark
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
 - ITBasicCallControl.Unpark
---

# ITBasicCallControl::Unpark


## -description

The 
<b>Unpark</b> method gets the call from park.



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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The park operation is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_INVALCALLSTATE</b></dt>
</dl>
</td>
<td width="60%">
Call state must be CS_IDLE.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>

## -remarks

To unpark a call, 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall">CreateCall</a> must be called using as the destination address the current parked location of the call. See the example below.


#### Examples


``` syntax
// Note: the parameters used in this call are obtained from elsewhere in the code.

HRESULT hr = pAddress->CreateCall( bstrAddressToCall,
                           dwAddressType,
                           dwMediaTypes,
                           &pBasicCall
                           );
// If ( hr != S_OK ) process the error here.

// Select appropriate terminals for call, and then call:
pBasicCall->Unpark();
```


## -see-also

<a href="/windows/desktop/Tapi/call-object">Call Object</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall">ITAddress::CreateCall</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol">ITBasicCallControl</a>



<a href="/windows/desktop/Tapi/park-ovr">Park overview</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkdirect">ParkDirect</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkindirect">ParkIndirect</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineunpark">lineUnpark</a>
