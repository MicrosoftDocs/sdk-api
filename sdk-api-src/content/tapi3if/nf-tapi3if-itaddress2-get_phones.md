---
UID: NF:tapi3if.ITAddress2.get_Phones
title: ITAddress2::get_Phones (tapi3if.h)
description: The get_Phones method returns a VARIANT pointer to an ITCollection of phone objects corresponding to the phone devices that can be used with this address.
helpviewer_keywords: ["ITAddress2 interface [TAPI 2.2]","get_Phones method","ITAddress2.get_Phones","ITAddress2::get_Phones","_tapi3_itaddress2_get_phones","get_Phones","get_Phones method [TAPI 2.2]","get_Phones method [TAPI 2.2]","ITAddress2 interface","tapi3.itaddress2_get_phones","tapi3if/ITAddress2::get_Phones"]
old-location: tapi3\itaddress2_get_phones.htm
tech.root: tapi3
ms.assetid: 5cd82f34-1f3f-46a2-bad3-954dc5b93d87
ms.date: 12/05/2018
ms.keywords: ITAddress2 interface [TAPI 2.2],get_Phones method, ITAddress2.get_Phones, ITAddress2::get_Phones, _tapi3_itaddress2_get_phones, get_Phones, get_Phones method [TAPI 2.2], get_Phones method [TAPI 2.2],ITAddress2 interface, tapi3.itaddress2_get_phones, tapi3if/ITAddress2::get_Phones
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
 - ITAddress2::get_Phones
 - tapi3if/ITAddress2::get_Phones
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
 - ITAddress2.get_Phones
---

# ITAddress2::get_Phones


## -description

The 
<b>get_Phones</b> method returns a VARIANT pointer to an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a> of phone objects corresponding to the phone devices that can be used with this address.

This method is intended for Visual Basic and scripting applications. C/C++ applications should use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress2-enumeratephones">EnumeratePhones</a> method instead.

## -parameters

### -param pPhones [out]

Pointer to a VARIANT containing an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a> of 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a> interface pointers.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A phone device declares itself as being available on all addresses that support audio terminals by the TSP setting the PHONEFEATURE_GENERICPHONE bit in the <b>dwPhoneFeatures</b> member of the 
<a href="/windows/desktop/api/tapi/ns-tapi-phonecaps">PHONECAPS</a> structure. A phone device can also declare itself as being preferred to an address or set of addresses by returning address/line IDs via 
<a href="/windows/desktop/api/tapi/nf-tapi-phonegetid">phoneGetID</a> with device class tapi/line. If no phones are available for use with the address, this method produces an empty collection and returns S_OK.

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a> interface returned by <b>ITAddress2::get_Phones</b>. The application must call <b>Release</b> on the 
<b>ITPhone</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress2-enumeratephones">EnumeratePhones</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress2">ITAddress2</a>