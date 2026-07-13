---
UID: NF:tapi3if.ITPhone.get_PhoneCapsString
title: ITPhone::get_PhoneCapsString (tapi3if.h)
description: The get_PhoneCapsString method gets a string capability/information about the phone, based on the PHONECAPS_STRING enum passed in. The application does not have to call ITPhone::Open before executing this method.
helpviewer_keywords: ["ITPhone interface [TAPI 2.2]","get_PhoneCapsString method","ITPhone.get_PhoneCapsString","ITPhone::get_PhoneCapsString","_tapi3_itphone_get_phonecapsstring","get_PhoneCapsString","get_PhoneCapsString method [TAPI 2.2]","get_PhoneCapsString method [TAPI 2.2]","ITPhone interface","tapi3.itphone_get_phonecapsstring","tapi3if/ITPhone::get_PhoneCapsString"]
old-location: tapi3\itphone_get_phonecapsstring.htm
tech.root: tapi3
ms.assetid: e4a0ed77-455e-428c-a3e5-cd467e47b5b2
ms.date: 12/05/2018
ms.keywords: ITPhone interface [TAPI 2.2],get_PhoneCapsString method, ITPhone.get_PhoneCapsString, ITPhone::get_PhoneCapsString, _tapi3_itphone_get_phonecapsstring, get_PhoneCapsString, get_PhoneCapsString method [TAPI 2.2], get_PhoneCapsString method [TAPI 2.2],ITPhone interface, tapi3.itphone_get_phonecapsstring, tapi3if/ITPhone::get_PhoneCapsString
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
 - ITPhone::get_PhoneCapsString
 - tapi3if/ITPhone::get_PhoneCapsString
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
 - ITPhone.get_PhoneCapsString
---

# ITPhone::get_PhoneCapsString


## -description

The 
<b>get_PhoneCapsString</b> method gets a string capability/information about the phone, based on the 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-phonecaps_string">PHONECAPS_STRING</a> enum passed in. The application does not have to call 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-open">ITPhone::Open</a> before executing this method.

## -parameters

### -param pcsCap [in]

The 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-phonecaps_string">PHONECAPS_STRING</a> descriptor for the phone capability.

### -param ppCapability [out]

Capability value. The <b>BSTR</b> is allocated using 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a>. The <b>BSTR</b> argument should be deallocated by the client.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a>



<a href="/windows/desktop/api/tapi/ns-tapi-phonecaps">PHONECAPS</a>