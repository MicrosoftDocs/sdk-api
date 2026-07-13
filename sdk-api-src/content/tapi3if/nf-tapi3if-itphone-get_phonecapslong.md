---
UID: NF:tapi3if.ITPhone.get_PhoneCapsLong
title: ITPhone::get_PhoneCapsLong (tapi3if.h)
description: The get_PhoneCapsLong method gets a DWORD capability of the phone, based on the PHONECAPS_LONG enum passed in. The application does not have to call ITPhone::Open before executing this method.
helpviewer_keywords: ["ITPhone interface [TAPI 2.2]","get_PhoneCapsLong method","ITPhone.get_PhoneCapsLong","ITPhone::get_PhoneCapsLong","_tapi3_itphone_get_phonecapslong","get_PhoneCapsLong","get_PhoneCapsLong method [TAPI 2.2]","get_PhoneCapsLong method [TAPI 2.2]","ITPhone interface","tapi3.itphone_get_phonecapslong","tapi3if/ITPhone::get_PhoneCapsLong"]
old-location: tapi3\itphone_get_phonecapslong.htm
tech.root: tapi3
ms.assetid: 9d7804a7-616b-4efc-9f3b-6d7b1fda1bf6
ms.date: 12/05/2018
ms.keywords: ITPhone interface [TAPI 2.2],get_PhoneCapsLong method, ITPhone.get_PhoneCapsLong, ITPhone::get_PhoneCapsLong, _tapi3_itphone_get_phonecapslong, get_PhoneCapsLong, get_PhoneCapsLong method [TAPI 2.2], get_PhoneCapsLong method [TAPI 2.2],ITPhone interface, tapi3.itphone_get_phonecapslong, tapi3if/ITPhone::get_PhoneCapsLong
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
 - ITPhone::get_PhoneCapsLong
 - tapi3if/ITPhone::get_PhoneCapsLong
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
 - ITPhone.get_PhoneCapsLong
---

# ITPhone::get_PhoneCapsLong


## -description

The 
<b>get_PhoneCapsLong</b> method gets a <b>DWORD</b> capability of the phone, based on the 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-phonecaps_long">PHONECAPS_LONG</a> enum passed in. The application does not have to call 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-open">ITPhone::Open</a> before executing this method.

## -parameters

### -param pclCap [in]

The 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-phonecaps_long">PHONECAPS_LONG</a> descriptor for the phone capability.

### -param plCapability [out]

Capability value.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a>



<a href="/windows/desktop/api/tapi/ns-tapi-phonecaps">PHONECAPS</a>