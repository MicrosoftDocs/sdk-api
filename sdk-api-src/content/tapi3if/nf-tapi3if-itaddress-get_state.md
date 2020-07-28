---
UID: NF:tapi3if.ITAddress.get_State
title: ITAddress::get_State (tapi3if.h)
description: The get_State method gets the current state of the address in pAddressState.
helpviewer_keywords: ["ITAddress interface [TAPI 2.2]","get_State method","ITAddress.get_State","ITAddress::get_State","_tapi3_itaddress_get_state","get_State","get_State method [TAPI 2.2]","get_State method [TAPI 2.2]","ITAddress interface","tapi3.itaddress_get_state","tapi3if/ITAddress::get_State"]
old-location: tapi3\itaddress_get_state.htm
tech.root: tapi3
ms.assetid: f68d0fb0-126d-4464-9d5a-0ffae4d40cb7
ms.date: 12/05/2018
ms.keywords: ITAddress interface [TAPI 2.2],get_State method, ITAddress.get_State, ITAddress::get_State, _tapi3_itaddress_get_state, get_State, get_State method [TAPI 2.2], get_State method [TAPI 2.2],ITAddress interface, tapi3.itaddress_get_state, tapi3if/ITAddress::get_State
f1_keywords:
- tapi3if/ITAddress.get_State
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Tapi3.dll
api_name:
- ITAddress.get_State
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITAddress::get_State


## -description


The 
<b>get_State</b> method gets the current state of the address in <i>pAddressState</i>.


## -parameters




### -param pAddressState [out]

Pointer to a member of 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-address_state">ADDRESS_STATE</a>.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pAddressState</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-address_state">ADDRESS_STATE</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/address-object">Address Object</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>
 

 

