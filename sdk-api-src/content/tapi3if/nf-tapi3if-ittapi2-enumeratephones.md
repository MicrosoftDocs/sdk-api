---
UID: NF:tapi3if.ITTAPI2.EnumeratePhones
title: ITTAPI2::EnumeratePhones (tapi3if.h)
description: The EnumeratePhones method enumerates the phone objects corresponding to the phone devices. If there are no phones available that can be used with the address, this method produces an empty enumeration and returns S_OK.
helpviewer_keywords: ["EnumeratePhones","EnumeratePhones method [TAPI 2.2]","EnumeratePhones method [TAPI 2.2]","ITTAPI2 interface","ITTAPI2 interface [TAPI 2.2]","EnumeratePhones method","ITTAPI2.EnumeratePhones","ITTAPI2::EnumeratePhones","_tapi3_ittapi2_enumeratephones","tapi3.ittapi2_enumeratephones","tapi3if/ITTAPI2::EnumeratePhones"]
old-location: tapi3\ittapi2_enumeratephones.htm
tech.root: tapi3
ms.assetid: 6b6aba8d-fbf7-459f-9bc8-79647194b989
ms.date: 12/05/2018
ms.keywords: EnumeratePhones, EnumeratePhones method [TAPI 2.2], EnumeratePhones method [TAPI 2.2],ITTAPI2 interface, ITTAPI2 interface [TAPI 2.2],EnumeratePhones method, ITTAPI2.EnumeratePhones, ITTAPI2::EnumeratePhones, _tapi3_ittapi2_enumeratephones, tapi3.ittapi2_enumeratephones, tapi3if/ITTAPI2::EnumeratePhones
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
 - ITTAPI2::EnumeratePhones
 - tapi3if/ITTAPI2::EnumeratePhones
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
 - ITTAPI2.EnumeratePhones
---

# ITTAPI2::EnumeratePhones


## -description

The 
<b>EnumeratePhones</b> method enumerates the phone objects corresponding to the phone devices. If there are no phones available that can be used with the address, this method produces an empty enumeration and returns S_OK.

This method is intended for C/C++ applications. Visual Basic and scripting applications must use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi2-get_phones">get_Phones</a> method.

## -parameters

### -param ppEnumPhone [out]

Pointer to an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone">IEnumPhone</a> interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone">IEnumPhone</a> interface returned by <b>ITTAPI2::EnumeratePhones</b>. The application must call <b>Release</b> on the 
<b>IEnumPhone</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone">IEnumPhone</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittapi2">ITTAPI2</a>