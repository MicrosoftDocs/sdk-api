---
UID: NF:tapi3if.ITPhone.EnumerateAddresses
title: ITPhone::EnumerateAddresses (tapi3if.h)
description: The EnumerateAddresses method enumerates the addresses that the phone can be used on. The application does not have to call ITPhone::Open before executing this method.
helpviewer_keywords: ["EnumerateAddresses","EnumerateAddresses method [TAPI 2.2]","EnumerateAddresses method [TAPI 2.2]","ITPhone interface","ITPhone interface [TAPI 2.2]","EnumerateAddresses method","ITPhone.EnumerateAddresses","ITPhone::EnumerateAddresses","_tapi3_itphone_enumerateaddresses","tapi3.itphone_enumerateaddresses","tapi3if/ITPhone::EnumerateAddresses"]
old-location: tapi3\itphone_enumerateaddresses.htm
tech.root: tapi3
ms.assetid: d72f6877-eb89-400e-a1bc-393116a9666f
ms.date: 12/05/2018
ms.keywords: EnumerateAddresses, EnumerateAddresses method [TAPI 2.2], EnumerateAddresses method [TAPI 2.2],ITPhone interface, ITPhone interface [TAPI 2.2],EnumerateAddresses method, ITPhone.EnumerateAddresses, ITPhone::EnumerateAddresses, _tapi3_itphone_enumerateaddresses, tapi3.itphone_enumerateaddresses, tapi3if/ITPhone::EnumerateAddresses
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
 - ITPhone::EnumerateAddresses
 - tapi3if/ITPhone::EnumerateAddresses
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
 - ITPhone.EnumerateAddresses
---

# ITPhone::EnumerateAddresses


## -description

The 
<b>EnumerateAddresses</b> method enumerates the addresses that the phone can be used on. The application does not have to call 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-open">ITPhone::Open</a> before executing this method.

This method is intended for C/C++ applications. Visual Basic and scripting applications must use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-get_addresses">get_Addresses</a> method.

## -parameters

### -param ppEnumAddress [out]

Pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumaddress">IEnumAddress</a> interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If no phones are available for use with the address, this method produces an empty enumeration and returns S_OK.

A phone device declares itself as being available on all addresses that support audio terminals by the TSP setting the PHONEFEATURE_GENERICPHONE bit in the <b>dwPhoneFeatures</b> member of the 
<a href="/windows/desktop/api/tapi/ns-tapi-phonecaps">PHONECAPS</a> structure. A phone device can also declare itself as being preferred to an address or set of addresses by returning address/line IDs using 
<a href="/windows/desktop/api/tapi/nf-tapi-phonegetid">phoneGetID</a> with device class tapi/line. The 
<b>EnumerateAddresses</b> method returns addresses that have been identified both ways.

To get only addresses that the phone is preferred on, you can call the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-enumeratepreferredaddresses">EnumeratePreferredAddresses</a> method.

A phone device declares itself as being specific to an address or set of addresses by returning address/line IDs using 
<a href="/windows/desktop/api/tapi/nf-tapi-phonegetid">phoneGetID</a> with device class tapi/line. Although the 
<a href="/windows/desktop/api/tapi/nf-tapi-phonegetid">phoneGetID</a> function requires the handle to an open phone device, the application does not have to call the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-open">ITPhone::Open</a> method before calling 
<b>EnumerateAddresses</b>. This is because the implementation of the phone object can open the phone and call 
<a href="/windows/desktop/api/tapi/nf-tapi-phonegetid">phoneGetID</a> during TAPI initialization or when a new phone object appears.

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumaddress">IEnumAddress</a> interface returned by <b>ITPhone::EnumerateAddresses</b>. The application must call <b>Release</b> on the 
<b>IEnumAddress</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-enumeratepreferredaddresses">EnumeratePreferredAddresses</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a>