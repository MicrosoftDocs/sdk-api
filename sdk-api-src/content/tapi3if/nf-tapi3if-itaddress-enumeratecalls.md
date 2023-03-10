---
UID: NF:tapi3if.ITAddress.EnumerateCalls
title: ITAddress::EnumerateCalls (tapi3if.h)
description: The EnumerateCalls method enumerates calls on the current address. This method is provided for C and C++ applications. Automation client applications, such as those written in Visual Basic, must use the get_Calls method.
helpviewer_keywords: ["EnumerateCalls","EnumerateCalls method [TAPI 2.2]","EnumerateCalls method [TAPI 2.2]","ITAddress interface","ITAddress interface [TAPI 2.2]","EnumerateCalls method","ITAddress.EnumerateCalls","ITAddress::EnumerateCalls","_tapi3_itaddress_enumeratecalls","tapi3.itaddress_enumeratecalls","tapi3if/ITAddress::EnumerateCalls"]
old-location: tapi3\itaddress_enumeratecalls.htm
tech.root: tapi3
ms.assetid: 2ffa90bf-3005-4fd0-b52f-b155c8b2194f
ms.date: 12/05/2018
ms.keywords: EnumerateCalls, EnumerateCalls method [TAPI 2.2], EnumerateCalls method [TAPI 2.2],ITAddress interface, ITAddress interface [TAPI 2.2],EnumerateCalls method, ITAddress.EnumerateCalls, ITAddress::EnumerateCalls, _tapi3_itaddress_enumeratecalls, tapi3.itaddress_enumeratecalls, tapi3if/ITAddress::EnumerateCalls
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
 - ITAddress::EnumerateCalls
 - tapi3if/ITAddress::EnumerateCalls
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
 - ITAddress.EnumerateCalls
---

# ITAddress::EnumerateCalls


## -description

The 
<b>EnumerateCalls</b> method enumerates calls on the current address. This method is provided for C and C++ applications. Automation client applications, such as those written in Visual Basic, must use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_calls">get_Calls</a> method.

## -parameters

### -param ppCallEnum [out]

Pointer to an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumcall">IEnumCall</a> interface.

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
The <i>ppCallEnum</i> parameter is not a valid pointer.

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
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumcall">IEnumCall</a> interface returned by <b>ITAddress::EnumerateCalls</b>. The application must call <b>Release</b> on the 
<b>IEnumCall</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumcall">IEnumCall</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_calls">ITAddress::get_Calls</a>