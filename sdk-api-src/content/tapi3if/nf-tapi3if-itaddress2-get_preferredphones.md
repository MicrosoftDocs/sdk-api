---
UID: NF:tapi3if.ITAddress2.get_PreferredPhones
title: ITAddress2::get_PreferredPhones (tapi3if.h)
description: The get_PreferredPhones method returns a collection of phone objects corresponding to the phone devices that are preferred for use with this address.
helpviewer_keywords: ["ITAddress2 interface [TAPI 2.2]","get_PreferredPhones method","ITAddress2.get_PreferredPhones","ITAddress2::get_PreferredPhones","_tapi3_itaddress2_get_preferredphones","get_PreferredPhones","get_PreferredPhones method [TAPI 2.2]","get_PreferredPhones method [TAPI 2.2]","ITAddress2 interface","tapi3.itaddress2_get_preferredphones","tapi3if/ITAddress2::get_PreferredPhones"]
old-location: tapi3\itaddress2_get_preferredphones.htm
tech.root: tapi3
ms.assetid: 6cb17c83-86db-4d44-bbd3-80a0e52fec73
ms.date: 12/05/2018
ms.keywords: ITAddress2 interface [TAPI 2.2],get_PreferredPhones method, ITAddress2.get_PreferredPhones, ITAddress2::get_PreferredPhones, _tapi3_itaddress2_get_preferredphones, get_PreferredPhones, get_PreferredPhones method [TAPI 2.2], get_PreferredPhones method [TAPI 2.2],ITAddress2 interface, tapi3.itaddress2_get_preferredphones, tapi3if/ITAddress2::get_PreferredPhones
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
 - ITAddress2::get_PreferredPhones
 - tapi3if/ITAddress2::get_PreferredPhones
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
 - ITAddress2.get_PreferredPhones
---

# ITAddress2::get_PreferredPhones


## -description

The 
<b>get_PreferredPhones</b> method returns a collection of phone objects corresponding to the phone devices that are preferred for use with this address.

This method is intended for Visual Basic and scripting applications. C/C++ applications should use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress2-enumeratepreferredphones">EnumeratePreferredPhones</a> method instead.

## -parameters

### -param pPhones [out]

Pointer to a <b>VARIANT</b> containing an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a> of 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a> interface pointers.

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
The <i>pPhones</i> parameter is not a valid pointer.

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

A phone device declares itself as being preferred to an address or set of addresses by returning address/line IDs using 
<a href="/windows/desktop/api/tapi/nf-tapi-phonegetid">phoneGetID</a> with device class tapi/line. If no phones are available for use with this address, the method produces an empty collection and returns S_OK.

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a> interface returned by <b>ITAddress2::get_PreferredPhones</b>. The application must call <b>Release</b> on the 
<b>ITPhone</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress2">ITAddress2</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a>