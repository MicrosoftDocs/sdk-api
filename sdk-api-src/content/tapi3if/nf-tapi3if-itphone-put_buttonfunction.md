---
UID: NF:tapi3if.ITPhone.put_ButtonFunction
title: ITPhone::put_ButtonFunction (tapi3if.h)
description: The put_ButtonFunction method sets the button function.
helpviewer_keywords: ["ITPhone interface [TAPI 2.2]","put_ButtonFunction method","ITPhone.put_ButtonFunction","ITPhone::put_ButtonFunction","_tapi3_itphone_put_buttonfunction","put_ButtonFunction","put_ButtonFunction method [TAPI 2.2]","put_ButtonFunction method [TAPI 2.2]","ITPhone interface","tapi3.itphone_put_buttonfunction","tapi3if/ITPhone::put_ButtonFunction"]
old-location: tapi3\itphone_put_buttonfunction.htm
tech.root: tapi3
ms.assetid: 8002ab8a-a15d-4a1f-b0c3-7a15c61cb6c4
ms.date: 12/05/2018
ms.keywords: ITPhone interface [TAPI 2.2],put_ButtonFunction method, ITPhone.put_ButtonFunction, ITPhone::put_ButtonFunction, _tapi3_itphone_put_buttonfunction, put_ButtonFunction, put_ButtonFunction method [TAPI 2.2], put_ButtonFunction method [TAPI 2.2],ITPhone interface, tapi3.itphone_put_buttonfunction, tapi3if/ITPhone::put_ButtonFunction
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
 - ITPhone::put_ButtonFunction
 - tapi3if/ITPhone::put_ButtonFunction
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
 - ITPhone.put_ButtonFunction
---

# ITPhone::put_ButtonFunction


## -description

The 
<b>put_ButtonFunction</b> method sets the button function.

## -parameters

### -param lButtonID [in]

Button identifier.

### -param ButtonFunction [in]

The 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-phone_button_function">PHONE_BUTTON_FUNCTION</a> descriptor for the button's function.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-get_buttonfunction">get_ButtonFunction</a>