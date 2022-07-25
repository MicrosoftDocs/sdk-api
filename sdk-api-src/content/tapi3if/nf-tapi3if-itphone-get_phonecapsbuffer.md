---
UID: NF:tapi3if.ITPhone.get_PhoneCapsBuffer
title: ITPhone::get_PhoneCapsBuffer (tapi3if.h)
description: The get_PhoneCapsBuffer method gets a buffer capability/information about the phone, based on the PHONECAPS_BUFFER enum passed in.
helpviewer_keywords: ["ITPhone interface [TAPI 2.2]","get_PhoneCapsBuffer method","ITPhone.get_PhoneCapsBuffer","ITPhone::get_PhoneCapsBuffer","_tapi3_itphone_get_phonecapsbuffer","get_PhoneCapsBuffer","get_PhoneCapsBuffer method [TAPI 2.2]","get_PhoneCapsBuffer method [TAPI 2.2]","ITPhone interface","tapi3.itphone_get_phonecapsbuffer","tapi3if/ITPhone::get_PhoneCapsBuffer"]
old-location: tapi3\itphone_get_phonecapsbuffer.htm
tech.root: tapi3
ms.assetid: d9397aa8-2be4-4775-8123-975bdd58a6b5
ms.date: 12/05/2018
ms.keywords: ITPhone interface [TAPI 2.2],get_PhoneCapsBuffer method, ITPhone.get_PhoneCapsBuffer, ITPhone::get_PhoneCapsBuffer, _tapi3_itphone_get_phonecapsbuffer, get_PhoneCapsBuffer, get_PhoneCapsBuffer method [TAPI 2.2], get_PhoneCapsBuffer method [TAPI 2.2],ITPhone interface, tapi3.itphone_get_phonecapsbuffer, tapi3if/ITPhone::get_PhoneCapsBuffer
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
 - ITPhone::get_PhoneCapsBuffer
 - tapi3if/ITPhone::get_PhoneCapsBuffer
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
 - ITPhone.get_PhoneCapsBuffer
---

# ITPhone::get_PhoneCapsBuffer


## -description

The 
<b>get_PhoneCapsBuffer</b> method gets a buffer capability/information about the phone, based on the 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-phonecaps_buffer">PHONECAPS_BUFFER</a> enum passed in.

This method is intended for Visual Basic and scripting applications. C/C++ applications must use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-getphonecapsbuffer">GetPhoneCapsBuffer</a> method.

## -parameters

### -param pcbCaps [in]

The 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-phonecaps_buffer">PHONECAPS_BUFFER</a> descriptor for the phone capability.

### -param pVarBuffer [out]

Pointer to VARIANT containing the capability value.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a>



<a href="/windows/desktop/api/tapi/ns-tapi-phonecaps">PHONECAPS</a>