---
UID: NF:tapi3if.ITTAPIObjectEvent.get_Address
title: ITTAPIObjectEvent::get_Address (tapi3if.h)
description: The get_Address method gets a pointer to the Address object on which the event occurred.
helpviewer_keywords: ["ITTAPIObjectEvent interface [TAPI 2.2]","get_Address method","ITTAPIObjectEvent.get_Address","ITTAPIObjectEvent::get_Address","_tapi3_ittapiobjectevent_get_address","get_Address","get_Address method [TAPI 2.2]","get_Address method [TAPI 2.2]","ITTAPIObjectEvent interface","tapi3.ittapiobjectevent_get_address","tapi3if/ITTAPIObjectEvent::get_Address"]
old-location: tapi3\ittapiobjectevent_get_address.htm
tech.root: tapi3
ms.assetid: dfe4ec23-42ae-4bb7-86cc-4d45d36b8817
ms.date: 12/05/2018
ms.keywords: ITTAPIObjectEvent interface [TAPI 2.2],get_Address method, ITTAPIObjectEvent.get_Address, ITTAPIObjectEvent::get_Address, _tapi3_ittapiobjectevent_get_address, get_Address, get_Address method [TAPI 2.2], get_Address method [TAPI 2.2],ITTAPIObjectEvent interface, tapi3.ittapiobjectevent_get_address, tapi3if/ITTAPIObjectEvent::get_Address
f1_keywords:
- tapi3if/ITTAPIObjectEvent.get_Address
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
- ITTAPIObjectEvent.get_Address
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITTAPIObjectEvent::get_Address


## -description


The 
<b>get_Address</b> method gets a pointer to the Address object on which the event occurred.


## -parameters




### -param ppAddress [out]

Pointer to an 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a> interface pointer.


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
The <i>ppAddress</i> parameter is not a valid pointer.

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
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a> interface returned by <b>ITTAPIObjectEvent::get_Address</b>. The application must call <b>Release</b> on the 
<b>ITAddress</b> interface to free resources associated with it.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent">ITTAPIObjectEvent</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/tapi-object">TAPI Object</a>
 

 

