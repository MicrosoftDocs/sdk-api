---
UID: NF:tapi3if.ITPhone.Close
title: ITPhone::Close (tapi3if.h)
description: The Close method closes this phone device. The phone device remains closed until the application calls the ITPhone::Open method. For more information, see the following Remarks section.
helpviewer_keywords: ["Close","Close method [TAPI 2.2]","Close method [TAPI 2.2]","ITPhone interface","ITPhone interface [TAPI 2.2]","Close method","ITPhone.Close","ITPhone::Close","_tapi3_itphone_close","tapi3.itphone_close","tapi3if/ITPhone::Close"]
old-location: tapi3\itphone_close.htm
tech.root: tapi3
ms.assetid: 1eae1a14-dd5e-4ba9-8e6e-71e9956cb3e3
ms.date: 12/05/2018
ms.keywords: Close, Close method [TAPI 2.2], Close method [TAPI 2.2],ITPhone interface, ITPhone interface [TAPI 2.2],Close method, ITPhone.Close, ITPhone::Close, _tapi3_itphone_close, tapi3.itphone_close, tapi3if/ITPhone::Close
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
 - ITPhone::Close
 - tapi3if/ITPhone::Close
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
 - ITPhone.Close
---

# ITPhone::Close


## -description

The 
<b>Close</b> method closes this phone device. The phone device remains closed until the application calls the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-open">ITPhone::Open</a> method. For more information, see the following Remarks section.

This method is analogous to the TAPI 2.<i>x</i>
<a href="/windows/desktop/api/tapi/nf-tapi-phoneopen">phoneOpen</a> function; please see the TAPI 2.<i>x</i> documentation for more information.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

While a phone is closed, the application does not receive events pertaining to the phone.

A phone must be open with owner privilege for the application to set the state of the phone. Querying the state of the phone can typically be done even if the phone is not open; for more details, see the individual methods of the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a> interface.

After the phone device has been successfully closed, any 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol">ITAutomatedPhoneControl</a> interface pointer obtained for this phone object is no longer valid.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a>
