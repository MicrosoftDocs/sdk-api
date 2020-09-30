---
UID: NF:tapi3if.ITTAPI.EnumerateAddresses
title: ITTAPI::EnumerateAddresses (tapi3if.h)
description: The EnumerateAddresses method enumerates the addresses that are currently available. Provided for C and C++ applications. Automation client applications, such as those written in Visual Basic, must use the get_Addresses method.
helpviewer_keywords: ["EnumerateAddresses","EnumerateAddresses method [TAPI 2.2]","EnumerateAddresses method [TAPI 2.2]","ITTAPI interface","ITTAPI interface [TAPI 2.2]","EnumerateAddresses method","ITTAPI.EnumerateAddresses","ITTAPI::EnumerateAddresses","_tapi3_ittapi_enumerateaddresses","tapi3.ittapi_enumerateaddresses","tapi3if/ITTAPI::EnumerateAddresses"]
old-location: tapi3\ittapi_enumerateaddresses.htm
tech.root: tapi3
ms.assetid: b40a2071-24bf-470c-bfba-de23317e8652
ms.date: 12/05/2018
ms.keywords: EnumerateAddresses, EnumerateAddresses method [TAPI 2.2], EnumerateAddresses method [TAPI 2.2],ITTAPI interface, ITTAPI interface [TAPI 2.2],EnumerateAddresses method, ITTAPI.EnumerateAddresses, ITTAPI::EnumerateAddresses, _tapi3_ittapi_enumerateaddresses, tapi3.ittapi_enumerateaddresses, tapi3if/ITTAPI::EnumerateAddresses
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
 - ITTAPI::EnumerateAddresses
 - tapi3if/ITTAPI::EnumerateAddresses
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
 - ITTAPI.EnumerateAddresses
---

# ITTAPI::EnumerateAddresses


## -description

The 
<b>EnumerateAddresses</b> method enumerates the addresses that are currently available. Provided for C and C++ applications. Automation client applications, such as those written in Visual Basic, must use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_addresses">get_Addresses</a> method.

## -parameters

### -param ppEnumAddress [out]

Pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumaddress">IEnumAddress</a> interface.

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
The <i>ppEnumAddress</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The TAPI object has not been initialized.

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

An application typically uses this enumeration to check the capabilities of each address and determine which are useful for current purposes.

If an expected address is not found, this may indicate that the appropriate service provider has not been installed or is not working correctly.

TAPI calls the <b>Addref</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumaddress">IEnumAddress</a> interface returned by <b>ITTAPI::EnumerateAddresses</b>. The application must call the <b>Release</b> method on the 
<b>IEnumAddress</b> interface to free resources associated with it.

If an address is created or removed during a TAPI session, the application will be notified through the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittapieventnotification">ITTAPIEventNotification</a> interface. If an address has been created, such as by installing a Plug and Play device, the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a> returns the <b>TE_ADDRESSCREATE</b> member of the 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapiobject_event">TAPIOBJECT_EVENT</a> enum. If an address is removed, <b>ITTAPIEventNotification::Event</b> returns <b>TE_ADDRESSREMOVE</b>. Calling 
<b>EnumerateAddresses</b> after these events will reflect the current addresses.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumaddress">IEnumAddress</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittapi">ITTAPI</a>



<a href="/windows/desktop/Tapi/register-events">Register Events code snippet</a>



<a href="/windows/desktop/Tapi/tapi-object">TAPI Object</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_addresses">get_Addresses</a>