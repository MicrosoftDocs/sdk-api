---
UID: NF:tapi3if.ITPhone.get_Addresses
title: ITPhone::get_Addresses (tapi3if.h)
description: The get_Addresses method returns a collection of addresses that the phone can be used on. The application does not have to call ITPhone::Open before executing this method.
helpviewer_keywords: ["ITPhone interface [TAPI 2.2]","get_Addresses method","ITPhone.get_Addresses","ITPhone::get_Addresses","_tapi3_itphone_get_addresses","get_Addresses","get_Addresses method [TAPI 2.2]","get_Addresses method [TAPI 2.2]","ITPhone interface","tapi3.itphone_get_addresses","tapi3if/ITPhone::get_Addresses"]
old-location: tapi3\itphone_get_addresses.htm
tech.root: tapi3
ms.assetid: 823db8d1-e4e3-4cfb-a864-5ad57a44ebc6
ms.date: 12/05/2018
ms.keywords: ITPhone interface [TAPI 2.2],get_Addresses method, ITPhone.get_Addresses, ITPhone::get_Addresses, _tapi3_itphone_get_addresses, get_Addresses, get_Addresses method [TAPI 2.2], get_Addresses method [TAPI 2.2],ITPhone interface, tapi3.itphone_get_addresses, tapi3if/ITPhone::get_Addresses
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
 - ITPhone::get_Addresses
 - tapi3if/ITPhone::get_Addresses
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
 - ITPhone.get_Addresses
---

# ITPhone::get_Addresses


## -description

The 
<b>get_Addresses</b> method returns a collection of addresses that the phone can be used on. The application does not have to call 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-open">ITPhone::Open</a> before executing this method.

This method is intended for Visual Basic and scripting applications. C/C++ applications should use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-enumerateaddresses">EnumerateAddresses</a> method instead.

## -parameters

### -param pAddresses [out]

Pointer to a VARIANT containing an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a> of 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a> interface pointers.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A phone device declares itself as being available on all addresses that support audio terminals by the TSP setting the PHONEFEATURE_GENERICPHONE bit in the <b>dwPhoneFeatures</b> member of the 
<a href="/windows/desktop/api/tapi/ns-tapi-phonecaps">PHONECAPS</a> structure. A phone device can also declare itself as being preferred to an address or set of addresses by returning address/line IDs using 
<a href="/windows/desktop/api/tapi/nf-tapi-phonegetid">phoneGetID</a> with device class tapi/line. The 
<b>get_Addresses</b> method returns addresses that have been identified both ways.

To get only addresses that the phone is preferred on, you can call the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-get_preferredaddresses">get_PreferredAddresses</a> method.

The application does not have to call the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-open">ITPhone::Open</a> method before calling 
<b>get_Addresses</b>. This is because the implementation of the phone object can open the phone and call 
<a href="/windows/desktop/api/tapi/nf-tapi-phonegetid">phoneGetID</a> during TAPI initialization or when a new phone object appears.

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a> interface returned by <b>ITPhone::get_Addresses</b>. The application must call <b>Release</b> on the 
<b>ITAddress</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-get_preferredaddresses">get_PreferredAddresses</a>