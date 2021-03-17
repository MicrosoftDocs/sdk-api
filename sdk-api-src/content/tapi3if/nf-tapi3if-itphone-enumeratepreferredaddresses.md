---
UID: NF:tapi3if.ITPhone.EnumeratePreferredAddresses
title: ITPhone::EnumeratePreferredAddresses (tapi3if.h)
description: The EnumeratePreferredAddresses method enumerates the preferred addresses for the phone object. The application does not have to call ITPhone::Open before executing this method.
helpviewer_keywords: ["EnumeratePreferredAddresses","EnumeratePreferredAddresses method [TAPI 2.2]","EnumeratePreferredAddresses method [TAPI 2.2]","ITPhone interface","ITPhone interface [TAPI 2.2]","EnumeratePreferredAddresses method","ITPhone.EnumeratePreferredAddresses","ITPhone::EnumeratePreferredAddresses","_tapi3_itphone_enumeratepreferredaddresses","tapi3.itphone_enumeratepreferredaddresses","tapi3if/ITPhone::EnumeratePreferredAddresses"]
old-location: tapi3\itphone_enumeratepreferredaddresses.htm
tech.root: tapi3
ms.assetid: 7bb15dc1-c1f0-4da5-8217-baedb45b70f7
ms.date: 12/05/2018
ms.keywords: EnumeratePreferredAddresses, EnumeratePreferredAddresses method [TAPI 2.2], EnumeratePreferredAddresses method [TAPI 2.2],ITPhone interface, ITPhone interface [TAPI 2.2],EnumeratePreferredAddresses method, ITPhone.EnumeratePreferredAddresses, ITPhone::EnumeratePreferredAddresses, _tapi3_itphone_enumeratepreferredaddresses, tapi3.itphone_enumeratepreferredaddresses, tapi3if/ITPhone::EnumeratePreferredAddresses
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
 - ITPhone::EnumeratePreferredAddresses
 - tapi3if/ITPhone::EnumeratePreferredAddresses
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
 - ITPhone.EnumeratePreferredAddresses
---

# ITPhone::EnumeratePreferredAddresses


## -description

The 
<b>EnumeratePreferredAddresses</b> method enumerates the preferred addresses for the phone object. The application does not have to call 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-open">ITPhone::Open</a> before executing this method.

This method is intended for C/C++ applications. Visual Basic and scripting applications must use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-get_addresses">get_Addresses</a> method.

## -parameters

### -param ppEnumAddress [out]

Pointer to a location where, on success, the method places a pointer to an enumeration object that contains the list of addresses. For more information, see the following Remarks section.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to allocate the enumeration object.

</td>
</tr>
</table>

## -remarks

If there are no usable addresses present on the system, this method produces an empty enumeration and returns S_OK.

A phone device declares itself as being preferred to an address or set of addresses by returning address/line IDs using the TAPI 2.x 
<a href="/windows/desktop/api/tapi/nf-tapi-phonegetid">phoneGetID</a> function with device class tapi/line.

Although the 
<a href="/windows/desktop/api/tapi/nf-tapi-phonegetid">phoneGetID</a> function requires the handle to an open phone device, the application does not have to call the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-open">ITPhone::Open</a> method before calling 
<b>EnumeratePreferredAddresses</b>. This is because the implementation of the phone object can open the phone and call 
<b>phoneGetID</b> during TAPI initialization or when a new phone object appears.

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumaddress">IEnumAddress</a> interface returned by <b>ITPhone::EnumeratePreferredAddresses</b>. The application must call <b>Release</b> on the 
<b>IEnumAddress</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-enumerateaddresses">EnumerateAddresses</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumaddress">IEnumAddress</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a>



<a href="/windows/desktop/api/tapi/nf-tapi-phonegetid">phoneGetID</a>