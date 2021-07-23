---
UID: NF:tapi3if.ITPhone.get_ButtonFunction
title: ITPhone::get_ButtonFunction (tapi3if.h)
description: The get_ButtonFunction method retrieves the button function associated with a particular button.
helpviewer_keywords: ["ITPhone interface [TAPI 2.2]","get_ButtonFunction method","ITPhone.get_ButtonFunction","ITPhone::get_ButtonFunction","_tapi3_itphone_get_buttonfunction","get_ButtonFunction","get_ButtonFunction method [TAPI 2.2]","get_ButtonFunction method [TAPI 2.2]","ITPhone interface","tapi3.itphone_get_buttonfunction","tapi3if/ITPhone::get_ButtonFunction"]
old-location: tapi3\itphone_get_buttonfunction.htm
tech.root: tapi3
ms.assetid: a884c0b4-141a-4f04-8cfb-7ae6b1ec11b3
ms.date: 12/05/2018
ms.keywords: ITPhone interface [TAPI 2.2],get_ButtonFunction method, ITPhone.get_ButtonFunction, ITPhone::get_ButtonFunction, _tapi3_itphone_get_buttonfunction, get_ButtonFunction, get_ButtonFunction method [TAPI 2.2], get_ButtonFunction method [TAPI 2.2],ITPhone interface, tapi3.itphone_get_buttonfunction, tapi3if/ITPhone::get_ButtonFunction
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
 - ITPhone::get_ButtonFunction
 - tapi3if/ITPhone::get_ButtonFunction
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
 - ITPhone.get_ButtonFunction
---

# ITPhone::get_ButtonFunction


## -description

The 
<b>get_ButtonFunction</b> method retrieves the button function associated with a particular button.

The application must call the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-open">ITPhone::Open</a> method before invoking this method; otherwise, the method fails.

## -parameters

### -param lButtonID [in]

Button identifier.

### -param pButtonFunction [out]

The 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-phone_button_function">PHONE_BUTTON_FUNCTION</a> descriptor for the button's function.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

See the description of the 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-phone_button_function">PHONE_BUTTON_FUNCTION</a> enum for a list of possible button functions.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-put_buttonfunction">put_ButtonFunction</a>