---
UID: NF:tapi3if.ITTAPI2.get_Phones
title: ITTAPI2::get_Phones (tapi3if.h)
description: The get_Phones method enumerates the phone objects corresponding to the phone devices. If there are no phones available that can be used with the address, this method produces an empty collection and returns S_OK.
helpviewer_keywords: ["ITTAPI2 interface [TAPI 2.2]","get_Phones method","ITTAPI2.get_Phones","ITTAPI2::get_Phones","_tapi3_ittapi2_get_phones","get_Phones","get_Phones method [TAPI 2.2]","get_Phones method [TAPI 2.2]","ITTAPI2 interface","tapi3.ittapi2_get_phones","tapi3if/ITTAPI2::get_Phones"]
old-location: tapi3\ittapi2_get_phones.htm
tech.root: tapi3
ms.assetid: 03fe03fc-c58d-4e2a-a187-5ab9a676e89e
ms.date: 12/05/2018
ms.keywords: ITTAPI2 interface [TAPI 2.2],get_Phones method, ITTAPI2.get_Phones, ITTAPI2::get_Phones, _tapi3_ittapi2_get_phones, get_Phones, get_Phones method [TAPI 2.2], get_Phones method [TAPI 2.2],ITTAPI2 interface, tapi3.ittapi2_get_phones, tapi3if/ITTAPI2::get_Phones
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
 - ITTAPI2::get_Phones
 - tapi3if/ITTAPI2::get_Phones
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
 - ITTAPI2.get_Phones
---

# ITTAPI2::get_Phones


## -description

The 
<b>get_Phones</b> method enumerates the phone objects corresponding to the phone devices. If there are no phones available that can be used with the address, this method produces an empty collection and returns S_OK.

This method is intended for Visual Basic and scripting applications. C/C++ applications will find the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi2-enumeratephones">EnumeratePhones</a> method more convenient.

## -parameters

### -param pPhones [out]

Pointer to a <b>VARIANT</b> containing an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a> of 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a> interface pointers.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a> interface returned by <b>ITTAPI2::get_Phones</b>. The application must call <b>Release</b> on the 
<b>ITPhone</b> interface to free resources associated with it.

## -see-also

<b>IEnumPhone</b>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittapi2">ITTAPI2</a>