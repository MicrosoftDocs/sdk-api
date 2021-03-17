---
UID: NF:tapi3if.ITPhone.get_PreferredAddresses
title: ITPhone::get_PreferredAddresses (tapi3if.h)
description: The get_PreferredAddresses method returns a collection of addresses that the phone is preferred for use on. The application does not have to call ITPhone::Open before executing this method.
helpviewer_keywords: ["ITPhone interface [TAPI 2.2]","get_PreferredAddresses method","ITPhone.get_PreferredAddresses","ITPhone::get_PreferredAddresses","_tapi3_itphone_get_preferredaddresses","get_PreferredAddresses","get_PreferredAddresses method [TAPI 2.2]","get_PreferredAddresses method [TAPI 2.2]","ITPhone interface","tapi3.itphone_get_preferredaddresses","tapi3if/ITPhone::get_PreferredAddresses"]
old-location: tapi3\itphone_get_preferredaddresses.htm
tech.root: tapi3
ms.assetid: bda43c65-a1f9-4143-b808-2a4e61220b1b
ms.date: 12/05/2018
ms.keywords: ITPhone interface [TAPI 2.2],get_PreferredAddresses method, ITPhone.get_PreferredAddresses, ITPhone::get_PreferredAddresses, _tapi3_itphone_get_preferredaddresses, get_PreferredAddresses, get_PreferredAddresses method [TAPI 2.2], get_PreferredAddresses method [TAPI 2.2],ITPhone interface, tapi3.itphone_get_preferredaddresses, tapi3if/ITPhone::get_PreferredAddresses
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
 - ITPhone::get_PreferredAddresses
 - tapi3if/ITPhone::get_PreferredAddresses
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
 - ITPhone.get_PreferredAddresses
---

# ITPhone::get_PreferredAddresses


## -description

The 
<b>get_PreferredAddresses</b> method returns a collection of addresses that the phone is preferred for use on. The application does not have to call 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-open">ITPhone::Open</a> before executing this method.

This method is intended for Visual Basic and scripting applications. C/C++ applications will find it more convenient to use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-enumerateaddresses">EnumerateAddresses</a> method.

## -parameters

### -param pAddresses [out]

Pointer to a <b>VARIANT</b> containing an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a> of 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a> interface pointers.

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
The <i>pAddresses</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to allocate the collection object.

</td>
</tr>
</table>

## -remarks

If no usable addresses are present on the system, this method returns an empty collection.

A phone device declares itself as being preferred to an address or set of addresses by returning address/line IDs using the TAPI 2.x 
<a href="/windows/desktop/api/tapi/nf-tapi-phonegetid">phoneGetID</a> function with device class tapi/line.

Although the 
<a href="/windows/desktop/api/tapi/nf-tapi-phonegetid">phoneGetID</a> function requires the handle to an open phone device, the application does not have to call the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-open">ITPhone::Open</a> method before calling 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-enumeratepreferredaddresses">EnumeratePreferredAddresses</a>. This is because the implementation of the phone object can open the phone and call 
<b>phoneGetID</b> during TAPI initialization or when a new phone object appears.

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a> interface returned by <b>ITPhone::get_PreferredAddresses</b>. The application must call <b>Release</b> on the 
<b>ITAddress</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-enumeratepreferredaddresses">EnumeratePreferredAddresses</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-get_addresses">get_Addresses</a>



<a href="/windows/desktop/api/tapi/nf-tapi-phonegetid">phoneGetID</a>