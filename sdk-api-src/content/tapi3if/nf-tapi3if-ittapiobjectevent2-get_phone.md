---
UID: NF:tapi3if.ITTAPIObjectEvent2.get_Phone
title: ITTAPIObjectEvent2::get_Phone (tapi3if.h)
description: The get_Phone method returns a pointer to the ITPhone interface on the phone object that caused this TAPI object event to be fired.
helpviewer_keywords: ["ITTAPIObjectEvent2 interface [TAPI 2.2]","get_Phone method","ITTAPIObjectEvent2.get_Phone","ITTAPIObjectEvent2::get_Phone","_tapi3_ittapiobjectevent2_get_phone","get_Phone","get_Phone method [TAPI 2.2]","get_Phone method [TAPI 2.2]","ITTAPIObjectEvent2 interface","tapi3.ittapiobjectevent2_get_phone","tapi3if/ITTAPIObjectEvent2::get_Phone"]
old-location: tapi3\ittapiobjectevent2_get_phone.htm
tech.root: tapi3
ms.assetid: 76e316f6-536b-4531-a4a6-397e258678cc
ms.date: 12/05/2018
ms.keywords: ITTAPIObjectEvent2 interface [TAPI 2.2],get_Phone method, ITTAPIObjectEvent2.get_Phone, ITTAPIObjectEvent2::get_Phone, _tapi3_ittapiobjectevent2_get_phone, get_Phone, get_Phone method [TAPI 2.2], get_Phone method [TAPI 2.2],ITTAPIObjectEvent2 interface, tapi3.ittapiobjectevent2_get_phone, tapi3if/ITTAPIObjectEvent2::get_Phone
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
 - ITTAPIObjectEvent2::get_Phone
 - tapi3if/ITTAPIObjectEvent2::get_Phone
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
 - ITTAPIObjectEvent2.get_Phone
---

# ITTAPIObjectEvent2::get_Phone


## -description

The 
<b>get_Phone</b> method returns a pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a> interface on the phone object that caused this TAPI object event to be fired.

## -parameters

### -param ppPhone [out]

Pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a> interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a> interface returned by <b>ITTAPIObjectEvent2::get_Phone</b>. The application must call <b>Release</b> on the 
<b>ITPhone</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent2">ITTAPIObjectEvent2</a>