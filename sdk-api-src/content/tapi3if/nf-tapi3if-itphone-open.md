---
UID: NF:tapi3if.ITPhone.Open
title: ITPhone::Open (tapi3if.h)
description: The Open method opens this phone device. The phone device remains open until the application calls ITPhone::Close or until TAPI is shut down.
helpviewer_keywords: ["ITPhone interface [TAPI 2.2]","Open method","ITPhone.Open","ITPhone::Open","Open","Open method [TAPI 2.2]","Open method [TAPI 2.2]","ITPhone interface","_tapi3_itphone_open","tapi3.itphone_open","tapi3if/ITPhone::Open"]
old-location: tapi3\itphone_open.htm
tech.root: tapi3
ms.assetid: d9efe2f7-3628-4e1f-b554-a6889d82a973
ms.date: 12/05/2018
ms.keywords: ITPhone interface [TAPI 2.2],Open method, ITPhone.Open, ITPhone::Open, Open, Open method [TAPI 2.2], Open method [TAPI 2.2],ITPhone interface, _tapi3_itphone_open, tapi3.itphone_open, tapi3if/ITPhone::Open
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
 - ITPhone::Open
 - tapi3if/ITPhone::Open
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
 - ITPhone.Open
---

# ITPhone::Open


## -description

The 
<b>Open</b> method opens this phone device. The phone device remains open until the application calls 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-close">ITPhone::Close</a> or until TAPI is shut down.

This method is analogous to the TAPI 2.<i>x</i>
<a href="/windows/desktop/api/tapi/nf-tapi-phoneopen">phoneOpen</a> function; please see the TAPI 2.<i>x</i> documentation for more information.

## -parameters

### -param Privilege [in]

The 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-phone_privilege">PHONE_PRIVILEGE</a> descriptor for the application's privilege status with respect to the phone device.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

While a phone is open, the application receives events pertaining to the phone.

Also, a phone must be open with owner privilege for the application to set the state of the phone. Querying the state of the phone can typically be done even if the phone is not open; for more details, see the individual methods of the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a> interface.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a>