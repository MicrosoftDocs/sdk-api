---
UID: NF:tapi3if.ITPhone.get_ButtonMode
title: ITPhone::get_ButtonMode (tapi3if.h)
description: The get_ButtonMode method retrieves the button mode associated with a particular button.
helpviewer_keywords: ["ITPhone interface [TAPI 2.2]","get_ButtonMode method","ITPhone.get_ButtonMode","ITPhone::get_ButtonMode","_tapi3_itphone_get_buttonmode","get_ButtonMode","get_ButtonMode method [TAPI 2.2]","get_ButtonMode method [TAPI 2.2]","ITPhone interface","tapi3.itphone_get_buttonmode","tapi3if/ITPhone::get_ButtonMode"]
old-location: tapi3\itphone_get_buttonmode.htm
tech.root: tapi3
ms.assetid: 5b3173bf-1c79-4c5d-a2bc-3b3ae4f0ae8a
ms.date: 12/05/2018
ms.keywords: ITPhone interface [TAPI 2.2],get_ButtonMode method, ITPhone.get_ButtonMode, ITPhone::get_ButtonMode, _tapi3_itphone_get_buttonmode, get_ButtonMode, get_ButtonMode method [TAPI 2.2], get_ButtonMode method [TAPI 2.2],ITPhone interface, tapi3.itphone_get_buttonmode, tapi3if/ITPhone::get_ButtonMode
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
 - ITPhone::get_ButtonMode
 - tapi3if/ITPhone::get_ButtonMode
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
 - ITPhone.get_ButtonMode
---

# ITPhone::get_ButtonMode


## -description

The 
<b>get_ButtonMode</b> method retrieves the button mode associated with a particular button.

The application must call 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-open">ITPhone::Open</a> before invoking this method; otherwise, the invocation fails.

## -parameters

### -param lButtonID [in]

Button identifier. For more information, see the following Remarks section.

### -param pButtonMode [out]

The 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-phone_button_mode">PHONE_BUTTON_MODE</a> descriptor for the button's mode.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

See the description of the 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-phone_button_mode">PHONE_BUTTON_MODE</a> enum and the TAPI 2.<i>x</i> documentation for more information about button modes.

The two following 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-phone_button_mode">PHONE_BUTTON_MODE</a> values are of particular interest:

<ol>
<li>If the 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-phone_button_mode">PHONE_BUTTON_MODE</a> value is PBM_FEATURE, the application should call the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-get_buttonfunction">get_ButtonFunction</a> to retrieve the specific meaning of the button.</li>
<li>If the 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-phone_button_mode">PHONE_BUTTON_MODE</a> value is PBM_KEYPAD, the button is a keypad button whose value is indicated by the value of the <i>lButtonID</i> parameter. For example, if <i>lButtonID</i> == 10 then the button is the * (star) key on the keypad.</li>
</ol>

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-get_buttonfunction">get_ButtonFunction</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-put_buttonmode">put_ButtonMode</a>