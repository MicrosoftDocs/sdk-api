---
UID: NF:tapi3if.ITPhone.GetPhoneCapsBuffer
title: ITPhone::GetPhoneCapsBuffer (tapi3if.h)
description: The GetPhoneCapsBuffer method gets a buffer capability/information about the phone, based on the PHONECAPS_BUFFER enum passed in.
helpviewer_keywords: ["GetPhoneCapsBuffer","GetPhoneCapsBuffer method [TAPI 2.2]","GetPhoneCapsBuffer method [TAPI 2.2]","ITPhone interface","ITPhone interface [TAPI 2.2]","GetPhoneCapsBuffer method","ITPhone.GetPhoneCapsBuffer","ITPhone::GetPhoneCapsBuffer","_tapi3_itphone_getphonecapsbuffer","tapi3.itphone_getphonecapsbuffer","tapi3if/ITPhone::GetPhoneCapsBuffer"]
old-location: tapi3\itphone_getphonecapsbuffer.htm
tech.root: tapi3
ms.assetid: 239902ca-0e9e-4b8d-927d-ee46a35dd9d8
ms.date: 12/05/2018
ms.keywords: GetPhoneCapsBuffer, GetPhoneCapsBuffer method [TAPI 2.2], GetPhoneCapsBuffer method [TAPI 2.2],ITPhone interface, ITPhone interface [TAPI 2.2],GetPhoneCapsBuffer method, ITPhone.GetPhoneCapsBuffer, ITPhone::GetPhoneCapsBuffer, _tapi3_itphone_getphonecapsbuffer, tapi3.itphone_getphonecapsbuffer, tapi3if/ITPhone::GetPhoneCapsBuffer
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
 - ITPhone::GetPhoneCapsBuffer
 - tapi3if/ITPhone::GetPhoneCapsBuffer
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
 - ITPhone.GetPhoneCapsBuffer
---

# ITPhone::GetPhoneCapsBuffer


## -description

The 
<b>GetPhoneCapsBuffer</b> method gets a buffer capability/information about the phone, based on the 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-phonecaps_buffer">PHONECAPS_BUFFER</a> enum passed in.

This method is intended for C/C++ applications. Visual Basic and scripting applications must use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-get_phonecapsbuffer">get_PhoneCapsBuffer</a> method.

## -parameters

### -param pcbCaps [in]

The 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-phonecaps_buffer">PHONECAPS_BUFFER</a> descriptor for the phone capability.

### -param pdwSize [out]

Size of the buffer, in bytes.

### -param ppPhoneCapsBuffer [out]

Pointer to the buffer containing the values.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a>



<a href="/windows/desktop/api/tapi/ns-tapi-phonecaps">PHONECAPS</a>